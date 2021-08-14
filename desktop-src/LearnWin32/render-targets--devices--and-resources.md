---
title: Destinos de representación, dispositivos y recursos
description: Destinos de representación, dispositivos y recursos
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381d6e696cc9dce47cc8dad05b0e546371d50c51012daba725eb08f20d247eae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387647"
---
# <a name="render-targets-devices-and-resources"></a>Destinos de representación, dispositivos y recursos

Un *destino de representación* es simplemente la ubicación donde se dibujará el programa. Normalmente, el destino de representación es una ventana (específicamente, el área de cliente de la ventana). También podría ser un mapa de bits en memoria que no se muestra. Un destino de representación se representa mediante la [**interfaz ID2D1RenderTarget.**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget)

Un *dispositivo* es una abstracción que representa lo que realmente dibuja los píxeles. Un dispositivo de hardware usa la GPU para un rendimiento más rápido, mientras que un dispositivo de software usa la CPU. La aplicación no crea el dispositivo. En su lugar, el dispositivo se crea implícitamente cuando la aplicación crea el destino de representación. Cada destino de representación está asociado a un dispositivo determinado, ya sea hardware o software.

![diagrama que muestra la relación entre un destino de representación y un dispositivo.](images/graphics09.png)

Un *recurso* es un objeto que el programa usa para dibujar. Estos son algunos ejemplos de recursos que se definen en Direct2D:

-   **Pincel**. Controla cómo se pintan las líneas y regiones. Los tipos de pincel incluyen pinceles de color sólido y pinceles de degradado.
-   **Estilo de trazo**. Controla la apariencia de una línea, por ejemplo, discontinua o sólida.
-   **Geometría**. Representa una colección de líneas y curvas.
-   **Malla**. Forma formada por triángulos. La GPU puede consumir datos de malla directamente, a diferencia de los datos de geometría, que se deben convertir antes de la representación.

Los destinos de representación también se consideran un tipo de recurso.

Algunos recursos se benefician de la aceleración de hardware. Un recurso de este tipo siempre está asociado a un dispositivo determinado, ya sea hardware (GPU) o software (CPU). Este tipo de recurso se denomina *dependiente del dispositivo.* Los pinceles y las mallas son ejemplos de recursos dependientes del dispositivo. Si el dispositivo deja de estar disponible, el recurso debe volver a crearse para un nuevo dispositivo.

Otros recursos se mantienen en la memoria de CPU, independientemente del dispositivo que se utilice. Estos recursos son *independientes del dispositivo,* porque no están asociados a un dispositivo determinado. No es necesario volver a crear recursos independientes del dispositivo cuando cambia el dispositivo. Los estilos de trazo y las geometrías son recursos independientes del dispositivo.

La documentación de MSDN de cada recurso indica si el recurso depende del dispositivo o es independiente del dispositivo. Cada tipo de recurso se representa mediante una interfaz que deriva de [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource). Por ejemplo, los pinceles se representan mediante la [**interfaz ID2D1Brush.**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush)

## <a name="the-direct2d-factory-object"></a>El objeto de generador de Direct2D

El primer paso al usar Direct2D es crear una instancia del objeto de generador de Direct2D. En la programación informática, *un generador* es un objeto que crea otros objetos. El generador de Direct2D crea los siguientes tipos de objetos:

-   Destinos de representación.
-   Recursos independientes del dispositivo, como estilos de trazo y geometrías.

El objeto de destino de representación crea recursos dependientes del dispositivo, como pinceles y mapas de bits.

![diagrama que muestra el generador de Direct2d.](images/graphics10.png)

Para crear el objeto de generador de Direct2D, llame a la [**función D2D1CreateFactory.**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



El primer parámetro es una marca que especifica las opciones de creación. La **marca D2D1 \_ FACTORY TYPE SINGLE \_ \_ \_ THREADED** significa que no llamará a Direct2D desde varios subprocesos. Para admitir llamadas desde varios subprocesos, especifique **D2D1 \_ FACTORY TYPE MULTI \_ \_ \_ THREADED**. Si el programa usa un único subproceso para llamar a Direct2D, la opción de un solo subproceso es más eficaz.

El segundo parámetro de la [**función D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) recibe un puntero a la [**interfaz ID2D1Factory.**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory)

Debe crear el objeto de generador de Direct2D antes del primer [**mensaje \_ DE WM PAINT.**](/windows/desktop/gdi/wm-paint) El controlador de mensajes [**\_ WM CREATE**](/windows/desktop/winmsg/wm-create) es un buen lugar para crear el generador:


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a>Creación de recursos de Direct2D

El programa Circle usa los siguientes recursos dependientes del dispositivo:

-   Destino de representación asociado a la ventana de la aplicación.
-   Pincel de color sólido para pintar el círculo.

Cada uno de estos recursos se representa mediante una interfaz COM:

-   La [**interfaz ID2D1HwndRenderTarget representa**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) el destino de representación.
-   La [**interfaz ID2D1SolidColorBrush representa**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) el pincel.

El programa Circle almacena punteros a estas interfaces como variables miembro de la `MainWindow` clase :


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



El código siguiente crea estos dos recursos.


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



Para crear un destino de representación para una ventana, llame al método [**ID2D1Factory::CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) en el generador de Direct2D.

-   El primer parámetro especifica opciones comunes a cualquier tipo de destino de representación. En este caso, pasaremos las opciones predeterminadas llamando a la función auxiliar [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).
-   El segundo parámetro especifica el identificador de la ventana más el tamaño del destino de representación, en píxeles.
-   El tercer parámetro recibe un [**puntero ID2D1HwndRenderTarget.**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget)

Para crear el pincel de color sólido, llame al método [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) en el destino de representación. El color se da como un valor [**D2D1 \_ COLOR \_ F.**](/windows/desktop/Direct2D/d2d1-color-f) Para obtener más información sobre los colores en Direct2D, vea [Using Color in Direct2D](using-color-in-direct2d.md).

Además, observe que si el destino de representación ya existe, el `CreateGraphicsResources` método devuelve **S \_ OK** sin hacer nada. El motivo de este diseño será claro en el tema siguiente.

## <a name="next"></a>Siguientes

[Dibujo con Direct2D](drawing-with-direct2d.md)

 

 