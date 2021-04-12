---
title: Destinos de representación, dispositivos y recursos
description: Destinos de representación, dispositivos y recursos
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeddd84e12c52e0fd0ae82dab8b5e8741a2e0891
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358905"
---
# <a name="render-targets-devices-and-resources"></a>Destinos de representación, dispositivos y recursos

Un *destino de representación* es simplemente la ubicación donde se dibujará el programa. Normalmente, el destino de representación es una ventana (concretamente, el área cliente de la ventana). También podría ser un mapa de bits en memoria que no se muestra. Un destino de representación se representa mediante la interfaz [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) .

Un *dispositivo* es una abstracción que representa lo que realmente dibuja los píxeles. Un dispositivo de hardware usa la GPU para obtener un rendimiento más rápido, mientras que un dispositivo de software usa la CPU. La aplicación no crea el dispositivo. En su lugar, el dispositivo se crea implícitamente cuando la aplicación crea el destino de representación. Cada destino de representación está asociado a un dispositivo determinado, ya sea hardware o software.

![diagrama que muestra la relación entre un destino de representación y un dispositivo.](images/graphics09.png)

Un *recurso* es un objeto que el programa utiliza para dibujar. Estos son algunos ejemplos de recursos que se definen en Direct2D:

-   **Pincel**. Controla cómo se dibujan las líneas y las regiones. Los tipos de pincel incluyen pinceles de color sólido y pinceles de degradado.
-   **Estilo de trazo**. Controla la apariencia de una línea, por ejemplo, discontinua o Solid.
-   **Geometría**. Representa una colección de líneas y curvas.
-   **Malla**. Forma formada por triángulos. Los datos de malla se pueden usar directamente en la GPU, a diferencia de los datos de geometría, que se deben convertir antes de la representación.

Los destinos de representación también se consideran un tipo de recurso.

Algunos recursos se benefician de la aceleración de hardware. Un recurso de este tipo siempre está asociado a un dispositivo determinado, ya sea hardware (GPU) o software (CPU). Este tipo de recurso se denomina *dependiente del dispositivo*. Los pinceles y las mallas son ejemplos de recursos dependientes del dispositivo. Si el dispositivo deja de estar disponible, se debe volver a crear el recurso para un dispositivo nuevo.

Otros recursos se mantienen en la memoria de la CPU, independientemente del dispositivo que se use. Estos recursos son *independientes del dispositivo*, ya que no están asociados a un dispositivo determinado. No es necesario volver a crear recursos independientes del dispositivo cuando cambia el dispositivo. Los estilos y las geometrías de trazo son recursos independientes del dispositivo.

La documentación de MSDN para cada recurso indica si el recurso es dependiente del dispositivo o independiente del dispositivo. Cada tipo de recurso se representa mediante una interfaz que se deriva de [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource). Por ejemplo, los pinceles se representan mediante la interfaz [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) .

## <a name="the-direct2d-factory-object"></a>Objeto de generador de Direct2D

El primer paso al usar Direct2D es crear una instancia del objeto de fábrica de Direct2D. En la programación de equipos, un *generador* es un objeto que crea otros objetos. El generador de Direct2D crea los siguientes tipos de objetos:

-   Destinos de representación.
-   Recursos independientes del dispositivo, como los estilos de trazo y las geometrías.

Los recursos dependientes del dispositivo, como los pinceles y los mapas de bits, se crean mediante el objeto de destino de representación.

![diagrama que muestra el generador de direct2d.](images/graphics10.png)

Para crear el objeto de generador de Direct2D, llame a la función [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



El primer parámetro es una marca que especifica las opciones de creación. La marca de **\_ \_ \_ un solo \_ subproceso de tipo de generador D2D1** significa que no se llamará a Direct2D desde varios subprocesos. Para admitir llamadas de varios subprocesos, especifique el tipo de generador de D2D1 de varios **\_ \_ \_ \_ subprocesos**. Si el programa usa un solo subproceso para llamar a Direct2D, la opción de un solo subproceso es más eficaz.

El segundo parámetro de la función [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) recibe un puntero a la interfaz [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) .

Debe crear el objeto de fábrica de Direct2D antes del primer mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) . El controlador de [**\_ creación**](/windows/desktop/winmsg/wm-create) de mensajes de WM es un buen lugar para crear el generador:


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a>Crear recursos de Direct2D

El programa círculo usa los siguientes recursos dependientes del dispositivo:

-   Destino de representación que está asociado a la ventana de la aplicación.
-   Pincel de color sólido para pintar el círculo.

Cada uno de estos recursos se representa mediante una interfaz COM:

-   La interfaz [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) representa el destino de representación.
-   La interfaz [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) representa el pincel.

El programa de círculo almacena punteros a estas interfaces como variables de miembro de la `MainWindow` clase:


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



En el código siguiente se crean estos dos recursos.


```C++
HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}
```



Para crear un destino de representación para una ventana, llame al método [**ID2D1Factory:: CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) en el generador de Direct2D.

-   El primer parámetro especifica las opciones que son comunes a cualquier tipo de destino de representación. Aquí, pasamos las opciones predeterminadas llamando a la función auxiliar [**D2D1:: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).
-   El segundo parámetro especifica el identificador de la ventana más el tamaño del destino de representación, en píxeles.
-   El tercer parámetro recibe un puntero [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) .

Para crear el pincel de color sólido, llame al método [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) en el destino de representación. El color se proporciona como un [**valor \_ \_ F de color D2D1**](/windows/desktop/Direct2D/d2d1-color-f) . Para obtener más información sobre los colores en Direct2D, vea [usar el color en direct2d](using-color-in-direct2d.md).

Además, tenga en cuenta que si el destino de representación ya existe, el `CreateGraphicsResources` método devuelve **S \_ correcto** sin hacer nada. El motivo de este diseño quedará claro en el siguiente tema.

## <a name="next"></a>Siguientes

[Dibujo con Direct2D](drawing-with-direct2d.md)

 

 