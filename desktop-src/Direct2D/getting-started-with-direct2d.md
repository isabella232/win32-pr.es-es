---
title: Guía de inicio rápido de Direct2D
description: Resume los pasos necesarios para dibujar con Direct2D y proporciona código de ejemplo.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D, ejemplo de código de rectángulo de dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f9c4f7ee6ca99feb3cf7169a59ce73ff3b8f8c62c08ddad88b9e5acf5d9a814
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260075"
---
# <a name="direct2d-quickstart"></a>Guía de inicio rápido de Direct2D

Direct2D es una API en modo inmediato de código nativo para crear gráficos 2D. En este tema se muestra cómo usar Direct2D dentro de una aplicación Win32 típica para dibujar en un **HWND.**

> [!Note]  
> Si desea crear una aplicación de Windows Store que use Direct2D, consulte el inicio rápido [de Direct2D Windows 8](direct2d-quickstart-with-device-context.md) tema.

 

Este tema contiene las siguientes secciones:

-   [Dibujar un rectángulo simple](#drawing-a-simple-rectangle)
-   [Paso 1: Incluir encabezado Direct2D](#step-1-include-direct2d-header)
-   [Paso 2: Crear una instancia de ID2D1Factory](#step-2-create-an-id2d1factory)
-   [Paso 3: Crear un ID2D1HwndRenderTarget](#step-3-create-an-id2d1hwndrendertarget)
-   [Paso 4: Crear un pincel](#step-4-create-a-brush)
-   [Paso 5: Dibujar el rectángulo](#step-5-draw-the-rectangle)
-   [Paso 6: Liberar recursos](#step-6-release-resources)
-   [Creación de una aplicación Direct2D simple](#create-a-simple-direct2d-application)
-   [Temas relacionados](#related-topics)

## <a name="drawing-a-simple-rectangle"></a>Dibujar un rectángulo simple

Para dibujar un rectángulo mediante [GDI,](/windows/desktop/gdi/windows-gdi)puede controlar el [**mensaje WM \_ PAINT,**](/windows/desktop/gdi/wm-paint) como se muestra en el código siguiente.


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



El código para dibujar el mismo rectángulo con Direct2D es similar: crea recursos de dibujo, describe una forma para dibujar, dibuja la forma y, a continuación, libera los recursos de dibujo. En las secciones siguientes se describe cada uno de estos pasos en detalle.

## <a name="step-1-include-direct2d-header"></a>Paso 1: Incluir encabezado Direct2D

Además de los encabezados necesarios para una aplicación Win32, incluya el encabezado d2d1.h.

## <a name="step-2-create-an-id2d1factory"></a>Paso 2: Crear una instancia de ID2D1Factory

Una de las primeras cosas que hace cualquier ejemplo de Direct2D es crear una [**instancia de ID2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



La [**interfaz ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) es el punto de partida para usar Direct2D; use una **instancia de ID2D1Factory** para crear recursos de Direct2D.

Al crear un generador, puede especificar si es multiproceso o de un solo subproceso. (Para obtener más información sobre los generadores multiproceso, vea los comentarios en la página de referencia [**de ID2D1Factory).**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) En este ejemplo se crea un generador de un solo subproceso.

En general, la aplicación debe crear el generador una vez y conservarlo durante la vida útil de la aplicación.

## <a name="step-3-create-an-id2d1hwndrendertarget"></a>Paso 3: Crear un ID2D1HwndRenderTarget

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



Un destino de representación es un dispositivo que puede realizar operaciones de dibujo y crear recursos de dibujo dependientes del dispositivo, como pinceles. Los distintos tipos de destinos de representación se representan en distintos dispositivos. En el ejemplo anterior se usa [**un ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), que se representa en una parte de la pantalla.

Cuando sea posible, un destino de representación usa la GPU para acelerar las operaciones de representación y crear recursos de dibujo. De lo contrario, el destino de representación usa la CPU para procesar las instrucciones de representación y crear recursos. (Puede modificar este comportamiento mediante las marcas [**D2D1 \_ RENDER TARGET \_ \_ TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) al crear el destino de representación).

El [**método CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) toma tres parámetros. El primer parámetro, una estructura [**\_ RENDER TARGET \_ \_ PROPERTIES de D2D1,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) especifica las opciones de visualización remota, si se debe forzar que el destino de representación se represente en software o hardware, y el valor de PPP. El código de este ejemplo usa la función [**auxiliar D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) para aceptar las propiedades de destino de representación predeterminadas.

El segundo parámetro, una estructura [**D2D1 \_ HWND \_ RENDER TARGET \_ \_ PROPERTIES,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) especifica el **HWND** en el que se representa el contenido, el tamaño inicial del destino de representación (en píxeles) y sus opciones de [**presentación.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options) En este ejemplo se [**usa la función auxiliar D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) para especificar un HWND y un tamaño inicial. Usa opciones de presentación predeterminadas.

El tercer parámetro es la dirección del puntero que recibe la referencia de destino de representación.

Cuando se crea un destino de representación y la aceleración de hardware está disponible, se asignan recursos en la GPU del equipo. Al crear un destino de representación una vez y conservarlo tanto como sea posible, se obtienen ventajas de rendimiento. La aplicación debe crear destinos de representación una vez y retenerlos durante la vida útil de la aplicación o hasta que se reciba el error [**D2DERR \_ RECREATE \_ TARGET.**](direct2d-error-codes.md) Cuando reciba este error, deberá volver a crear el destino de representación (y los recursos que creó).

## <a name="step-4-create-a-brush"></a>Paso 4: Crear un pincel

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

Direct2D también proporciona otros tipos de pinceles: pinceles de degradado para pintar degradados radiales y lineales, y un pincel de mapa de bits para pintar con mapas de bits y patrones.

Algunas API de dibujo proporcionan lápices para dibujar contornos y pinceles para rellenar formas. Direct2D es diferente: no proporciona un objeto de lápiz, sino que usa un pincel para dibujar contornos y rellenar formas. Al dibujar contornos, use la interfaz [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) con un pincel para controlar las operaciones de acariciamiento de ruta de acceso.

Un pincel solo se puede usar con el destino de representación que lo creó y con otros destinos de representación en el mismo dominio de recursos. En general, debe crear pinceles una vez y conservarlos durante la vida útil del destino de representación que los creó. [**ID2D1SolidColorBrush es**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) la excepción única; Dado que es relativamente económico crearlo, puede crear un **objeto ID2D1SolidColorBrush** cada vez que dibuje un marco, sin que se note el rendimiento. También puede usar un único **ID2D1SolidColorBrush** y cambiar su color cada vez que lo use.

## <a name="step-5-draw-the-rectangle"></a>Paso 5: Dibujar el rectángulo

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



El [**método DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) toma dos parámetros: el rectángulo que se va a dibujar y el pincel que se va a usar para pintar el contorno del rectángulo. Opcionalmente, también puede especificar el ancho del trazo, el patrón de guión, la combinación de líneas y las opciones de extremo.

Debe llamar al [**método BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir los comandos de dibujo y debe llamar al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) una vez que haya terminado de emitir comandos de dibujo. El **método EndDraw** devuelve **un HRESULT** que indica si los comandos de dibujo se ejecutaron correctamente.

## <a name="step-6-release-resources"></a>Paso 6: Liberar recursos

Cuando no haya más fotogramas para dibujar o cuando reciba el error [**D2DERR \_ RECREATE \_ TARGET,**](direct2d-error-codes.md) libere el destino de representación y los dispositivos que creó.


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



Cuando la aplicación haya terminado de usar recursos de Direct2D (por ejemplo, cuando esté a punto de salir), libere el generador de Direct2D.


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a>Creación de una aplicación Direct2D simple

El código de este tema muestra los elementos básicos de una aplicación de Direct2D. Por brevedad, el tema omite el marco de trabajo de la aplicación y el código de control de errores que es característica de una aplicación bien escrita. Para obtener un tutorial más detallado que muestre el código completo para crear una aplicación direct2D sencilla y muestre los procedimientos recomendados de diseño, consulte Creación de una aplicación [direct2D simple.](direct2d-quickstart.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de una aplicación Direct2D simple](direct2d-quickstart.md)
</dt> </dl>

 

 