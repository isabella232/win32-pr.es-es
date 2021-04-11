---
title: Inicio rápido de Direct2D
description: Resume los pasos necesarios para dibujar con Direct2D y proporciona código de ejemplo.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Ejemplo de código de rectángulo de Direct2D, dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa59d7da057a7a9922e270d83937307762b06a40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149300"
---
# <a name="direct2d-quickstart"></a>Inicio rápido de Direct2D

Direct2D es una API de modo inmediato y de código nativo para crear gráficos 2D. En este tema se muestra cómo usar Direct2D en una aplicación Win32 típica para dibujar en un **hWnd**.

> [!Note]  
> Si quiere crear una aplicación de la tienda Windows que use Direct2D, vea el tema [de inicio rápido de direct2d para Windows 8](direct2d-quickstart-with-device-context.md) .

 

Este tema contiene las siguientes secciones:

-   [Dibujar un rectángulo simple](#drawing-a-simple-rectangle)
-   [Paso 1: incluir el encabezado de Direct2D](#step-1-include-direct2d-header)
-   [Paso 2: creación de un ID2D1Factory](#step-2-create-an-id2d1factory)
-   [Paso 3: creación de un ID2D1HwndRenderTarget](#step-3-create-an-id2d1hwndrendertarget)
-   [Paso 4: crear un pincel](#step-4-create-a-brush)
-   [Paso 5: dibujo del rectángulo](#step-5-draw-the-rectangle)
-   [Paso 6: liberar recursos](#step-6-release-resources)
-   [Creación de una aplicación de Direct2D sencilla](#create-a-simple-direct2d-application)
-   [Temas relacionados](#related-topics)

## <a name="drawing-a-simple-rectangle"></a>Dibujar un rectángulo simple

Para dibujar un rectángulo mediante [GDI](/windows/desktop/gdi/windows-gdi), podría controlar el mensaje [**de \_ dibujo de WM**](/windows/desktop/gdi/wm-paint) , tal y como se muestra en el código siguiente.


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



El código para dibujar el mismo rectángulo con Direct2D es similar: crea recursos de dibujo, describe una forma para dibujar, dibuja la forma y, a continuación, libera los recursos de dibujo. En las secciones siguientes se describe detalladamente cada uno de estos pasos.

## <a name="step-1-include-direct2d-header"></a>Paso 1: incluir el encabezado de Direct2D

Además de los encabezados necesarios para una aplicación Win32, incluya el encabezado d2d1. h.

## <a name="step-2-create-an-id2d1factory"></a>Paso 2: creación de un ID2D1Factory

Una de las primeras cosas que hace cualquier ejemplo de Direct2D es crear un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



La interfaz [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) es el punto de partida para usar Direct2D; Use un **ID2D1Factory** para crear recursos de Direct2D.

Al crear una factoría, puede especificar si es multiproceso o de un solo subproceso. (Para obtener más información sobre los generadores multiproceso, consulte la sección Comentarios en la [**Página de referencia de ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)). En este ejemplo se crea un generador de un solo subproceso.

En general, la aplicación debe crear el generador una vez y conservarlo durante la vida de la aplicación.

## <a name="step-3-create-an-id2d1hwndrendertarget"></a>Paso 3: creación de un ID2D1HwndRenderTarget

Después de crear un generador, úselo para crear un destino de representación.


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



Un destino de representación es un dispositivo que puede realizar operaciones de dibujo y crear recursos de dibujo dependientes del dispositivo, como pinceles. Los distintos tipos de destinos de representación se representan en distintos dispositivos. En el ejemplo anterior se usa un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), que se representa en una parte de la pantalla.

Cuando es posible, un destino de representación usa la GPU para acelerar las operaciones de representación y crear recursos de dibujo. De lo contrario, el destino de representación utiliza la CPU para procesar las instrucciones de representación y crear recursos. (Puede modificar este comportamiento mediante las marcas de [**\_ tipo de \_ destino \_ de representación de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) al crear el destino de representación).

El método [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) toma tres parámetros. El primer parámetro, un struct de propiedades de destino de representación de D2D1, especifica las opciones de pantalla remotas, si se debe forzar el destino de representación para que se represente en el software o hardware, y en el PPP. [**\_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) El código de este ejemplo usa la función auxiliar [**D2D1:: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) para aceptar las propiedades de destino de representación predeterminadas.

El segundo parámetro, un struct de [**propiedades de destino de representación de D2D1 \_ hWnd \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) , especifica el **hWnd** en el que se representa el contenido, el tamaño inicial del destino de representación (en píxeles) y sus [**Opciones de presentación**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options). En este ejemplo se usa la función auxiliar [**D2D1:: HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) para especificar un HWND y el tamaño inicial. Usa las opciones de presentación predeterminadas.

El tercer parámetro es la dirección del puntero que recibe la referencia de destino de representación.

Cuando se crea un destino de representación y la aceleración de hardware está disponible, se asignan recursos en la GPU del equipo. Al crear un destino de representación una vez y conservarlo lo máximo posible, se obtienen ventajas de rendimiento. La aplicación debe crear los destinos de representación una vez y conservarlos durante la vida de la aplicación o hasta que se reciba el error de [**\_ \_ destino de recreación de D2DERR**](direct2d-error-codes.md) . Cuando reciba este error, deberá volver a crear el destino de representación (y los recursos que haya creado).

## <a name="step-4-create-a-brush"></a>Paso 4: crear un pincel

Al igual que un generador, un destino de representación puede crear recursos de dibujo. En este ejemplo, el destino de representación crea un pincel.


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



Un pincel es un objeto que pinta un área, como el trazo de una forma o el relleno de una geometría. El pincel de este ejemplo pinta un área con un color sólido predefinido, negro.

Direct2D también proporciona otros tipos de pinceles: pinceles de degradado para pintar degradados lineales y radiales, y un pincel de mapa de bits para dibujar con mapas de bits y patrones.

Algunas API de dibujo proporcionan lápices para dibujar contornos y pinceles para rellenar formas. Direct2D es diferente: no proporciona un objeto Pen, sino que usa un pincel para dibujar contornos y formas de relleno. Al dibujar contornos, utilice la interfaz [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) con un pincel para controlar las operaciones de trazado de trazados.

Un pincel solo se puede usar con el destino de representación que lo creó y con otros destinos de representación en el mismo dominio de recursos. En general, debe crear pinceles una vez y conservarlos durante la vida del destino de representación que los creó. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) es la única excepción; Dado que es relativamente económico crearlo, puede crear un **ID2D1SolidColorBrush** cada vez que dibuje un fotograma, sin que se produzca ningún impacto apreciable en el rendimiento. También puede usar un solo **ID2D1SolidColorBrush** y cambiar su color cada vez que lo use.

## <a name="step-5-draw-the-rectangle"></a>Paso 5: dibujo del rectángulo

A continuación, use el destino de representación para dibujar el rectángulo.


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



El método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) toma dos parámetros: el rectángulo que se va a dibujar y el pincel que se va a usar para pintar el contorno del rectángulo. Opcionalmente, también puede especificar las opciones ancho del trazo, patrón de guión, combinación de líneas y límite final.

Debe llamar al método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir cualquier comando de dibujo y debe llamar al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) una vez que haya terminado de emitir comandos de dibujo. El método **EndDraw** devuelve un **valor HRESULT** que indica si los comandos de dibujo se realizaron correctamente.

## <a name="step-6-release-resources"></a>Paso 6: liberar recursos

Cuando no haya más fotogramas para dibujar, o cuando reciba el error de [**\_ \_ destino de recreación de D2DERR**](direct2d-error-codes.md) , libere el destino de representación y los dispositivos que creó.


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



Cuando la aplicación haya terminado de usar recursos de Direct2D (como cuando esté a punto de salir), libere el generador de Direct2D.


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a>Creación de una aplicación de Direct2D sencilla

En el código de este tema se muestran los elementos básicos de una aplicación de Direct2D. Por motivos de brevedad, el tema omite el marco de trabajo de la aplicación y el código de control de errores que es característico de una aplicación bien escrita. Para ver un tutorial más detallado en el que se muestra el código completo para crear una aplicación de Direct2D simple y se muestran las prácticas de diseño más adecuadas, consulte [creación de una aplicación de Direct2d simple](direct2d-quickstart.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una aplicación de Direct2D simple](direct2d-quickstart.md)
</dt> </dl>

 

 