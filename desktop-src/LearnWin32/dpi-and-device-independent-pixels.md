---
title: PPP y Device-Independent píxeles
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 'Más información sobre: PPP y Device-Independent píxeles'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6f04e1a056611fcdfe8b59ff65b38ecec99eaf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159993"
---
# <a name="dpi-and-device-independent-pixels"></a>PPP y Device-Independent píxeles

Para programar eficazmente con Windows gráficos, debe comprender dos conceptos relacionados:

-   Puntos por pulgada (PPP)
-   Píxeles independientes del dispositivo (DIP).

Empecemos con PPP. Esto requerirá un breve desviado a la tipografía. En tipografía, el tamaño de tipo se mide en unidades denominadas *puntos*. Un punto es igual a 1/72 de pulgada.

<dl> 1 pt = 1/72 pulgadas  
</dl>

> [!Note]  
> Esta es la definición de punto de publicación de escritorio. Históricamente, la medida exacta de un punto ha variado.

 

Por ejemplo, una fuente de 12 puntos está diseñada para caber dentro de una línea de texto de 1/6" (12/72). Obviamente, esto no significa que todos los caracteres de la fuente tienen exactamente 1/6" de alto. De hecho, algunos caracteres podrían ser más altos que 1/6". Por ejemplo, en muchas fuentes, el carácter A es más alto que el alto nominal de la fuente. Para mostrarse correctamente, la fuente necesita algo de espacio adicional entre el texto. Este espacio se denomina *el inicial.*

En la ilustración siguiente se muestra una fuente de 72 puntos. Las líneas sólidas muestran un rectángulo delimitador de 1" de alto alrededor del texto. La línea discontinua se denomina línea *base.* La mayoría de los caracteres de una fuente se encuentra en la línea base. El alto de la fuente incluye la parte por encima de la línea base (el aumento *)* y la parte por debajo de la línea base (el *descenso*). En la fuente que se muestra aquí, la subida es de 56 puntos y el descenso es de 16 puntos.

![ilustración que muestra una fuente de 72 puntos.](images/graphics11.png)

Sin embargo, cuando se trata de una pantalla de equipo, medir el tamaño del texto es problemático, ya que los píxeles no tienen el mismo tamaño. El tamaño de un píxel depende de dos factores: la resolución de pantalla y el tamaño físico del monitor. Por lo tanto, las pulgadas físicas no son una medida útil, ya que no hay ninguna relación fija entre pulgadas físicas y píxeles. En su lugar, las fuentes se miden en *unidades* lógicas. Una fuente de 72 puntos se define para tener una pulgada lógica de alto. A continuación, las pulgadas lógicas se convierten en píxeles. Durante muchos años, Windows la conversión siguiente: una pulgada lógica es igual a 96 píxeles. Con este factor de escalado, una fuente de 72 puntos se representa como 96 píxeles de alto. Una fuente de 12 puntos tiene 16 píxeles de alto.

<dl> 12 puntos = 12/72 pulgadas lógicas = 1/6 pulgada lógica = 96/6 píxeles = 16 píxeles  
</dl>

Este factor de escalado se describe como 96 puntos por pulgada (PPP). El término dots deriva de la impresión, donde los puntos físicos de la entrada de lápiz se ponen en el papel. Para las pantallas del equipo, sería más preciso decir 96 píxeles por pulgada lógica, pero el término PPP se ha bloqueado.

Dado que los tamaños de píxel reales varían, el texto que se puede leer en un monitor podría ser demasiado pequeño en otro monitor. Además, las personas tienen preferencias diferentes: algunas personas prefieren texto más grande. Por este motivo, Windows permite al usuario cambiar la configuración de PPP. Por ejemplo, si el usuario establece la pantalla en 144 PPP, una fuente de 72 puntos tiene una altura de 144 píxeles. La configuración de PPP estándar es 100 % (96 PPP), 125 % (120 PPP) y 150 % (144 PPP). El usuario también puede aplicar una configuración personalizada. A partir Windows 7, PPP es una configuración por usuario.

## <a name="dwm-scaling"></a>Escalado de DWM

Si un programa no tiene en cuenta ppp, los defectos siguientes pueden ser evidentes en la configuración de valores altos de PPP:

-   Elementos de interfaz de usuario recortados.
-   Diseño incorrecto.
-   Iconos y mapas de bits pixelados.
-   Coordenadas incorrectas del mouse, que pueden afectar a las pruebas de impacto, arrastrar y colocar, etc.

Para asegurarse de que los programas anteriores funcionan con valores altos de PPP, DWM implementa una reserva útil. Si un programa no está marcado como compatible con PPP, DWM escalará toda la interfaz de usuario para que coincida con la configuración de PPP. Por ejemplo, a 144 PPP, la interfaz de usuario se escala en un 150 %, incluido el texto, los gráficos, los controles y los tamaños de ventana. Si el programa crea una ventana de 500 × 500, la ventana aparece realmente como 750 × 750 píxeles y el contenido de la ventana se escala en consecuencia.

Este comportamiento significa que los programas anteriores "simplemente funcionan" con valores altos de PPP. Sin embargo, el escalado también da como resultado un aspecto algo desenfocado, ya que el escalado se aplica después de dibujar la ventana.

## <a name="dpi-aware-applications"></a>DPI-Aware aplicaciones

Para evitar el escalado de DWM, un programa puede marcarse como compatible con PPP. Esto indica al DWM que no realice ningún escalado automático de PPP. Todas las aplicaciones nuevas deben diseñarse para que sean con reconocimiento de PPP, ya que el reconocimiento de PPP mejora la apariencia de la interfaz de usuario en una configuración de PPP superior.

Un programa se declara a sí mismo compatible con PPP a través de su manifiesto de aplicación. Un *manifiesto* es simplemente un archivo XML que describe un archivo DLL o una aplicación. El manifiesto se incrusta normalmente en el archivo ejecutable, aunque se puede proporcionar como un archivo independiente. Un manifiesto contiene información como las dependencias dll, el nivel de privilegio solicitado y la versión de Windows para la que se diseñó el programa.

Para declarar que el programa es compatible con PPP, incluya la siguiente información en el manifiesto.

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

La lista que se muestra aquí es solo un manifiesto parcial, pero el vinculador Visual Studio genera automáticamente el resto del manifiesto. Para incluir un manifiesto parcial en el proyecto, realice los pasos siguientes en Visual Studio.

1.  En el menú **Project,** haga clic en **Propiedad**.
2.  En el panel izquierdo, expanda **Propiedades de configuración,** expanda **Herramienta manifiesto** y, a continuación, haga clic en Entrada **y salida.**
3.  En el **cuadro de texto Archivos de** manifiesto adicionales, escriba el nombre del archivo de manifiesto y, a continuación, haga clic en **Aceptar.**

Al marcar el programa como compatible con PPP, le está diciendo al DWM que no escale la ventana de la aplicación. Ahora, si crea una ventana de 500 × 500, la ventana ocupará 500 × 500 píxeles, independientemente de la configuración de PPP del usuario.

## <a name="gdi-and-dpi"></a>GDI y PPP

El dibujo GDI se mide en píxeles. Esto significa que si el programa está marcado como compatible con PPP y pide a GDI que dibuje un rectángulo de 200 × 100, el rectángulo resultante tendrá 200 píxeles de ancho y 100 píxeles de alto en la pantalla. Sin embargo, los tamaños de fuente GDI se escalan a la configuración de PPP actual. En otras palabras, si crea una fuente de 72 puntos, el tamaño de la fuente será de 96 píxeles a 96 PPP, pero de 144 píxeles a 144 PPP. Esta es una fuente de 72 puntos que se representa a 144 PPP mediante GDI.

![diagrama que muestra el escalado de fuentes de ppp en gdi.](images/graphics12.png)

Si la aplicación es compatible con PPP y usa GDI para dibujar, escale todas las coordenadas de dibujo para que coincidan con el valor de PPP.

## <a name="direct2d-and-dpi"></a>Direct2D y PPP

Direct2D realiza automáticamente el escalado para que coincida con la configuración de PPP. En Direct2D, las coordenadas se miden en unidades denominadas *píxeles independientes* del dispositivo (DIP). Una DIP se define como 1/96 de una *pulgada* lógica. En Direct2D, todas las operaciones de dibujo se especifican en DIP y, a continuación, se escalan a la configuración de PPP actual.



| Configuración de PPP | Tamaño de DIP    |
|-------------|-------------|
| 96          | 1 píxel     |
| 120         | 1,25 píxeles |
| 144         | 1,5 píxeles  |



 

Por ejemplo, si el valor de PPP del usuario es 144 PPP y pide a Direct2D que dibuje un rectángulo de 200 × 100, el rectángulo será de 300 × 150 píxeles físicos. Además, DirectWrite tamaños de fuente en DIP, en lugar de puntos. Para crear una fuente de 12 puntos, especifique 16 DIP (12 puntos = 1/6 pulgadas lógicas = 96/6 DIP). Cuando el texto se dibuja en la pantalla, Direct2D convierte los DIP en píxeles físicos. La ventaja de este sistema es que las unidades de medida son coherentes para el texto y el dibujo, independientemente de la configuración de PPP actual.

Una palabra de precaución: las coordenadas del mouse y la ventana se siguen dando en píxeles físicos, no en DIP. Por ejemplo, si procesa el mensaje [**\_ WM LBUTTONDOWN,**](/windows/desktop/inputdev/wm-lbuttondown) la posición del mouse hacia abajo se indica en píxeles físicos. Para dibujar un punto en esa posición, debe convertir las coordenadas de píxel en DIP.

## <a name="converting-physical-pixels-to-dips"></a>Conversión de píxeles físicos en DIP

La conversión de píxeles físicos a DIP usa la fórmula siguiente.

<dl> DIP = píxeles / (PPP/96,0)  
</dl>

Para obtener la configuración de PPP, llame al [**método ID2D1Factory::GetDesktopDpi.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) El valor de PPP se devuelve como dos valores de punto flotante, uno para el eje X y otro para el eje Y. En teoría, estos valores pueden diferir. Calcule un factor de escalado independiente para cada eje.


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



Esta es una manera alternativa de obtener la configuración de PPP si no usa Direct2D:


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> En Windows 10, versión 1903, [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) está en desuso y la recomendación es [**DisplayInformation::LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) para aplicaciones de la Tienda Windows o [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) para aplicaciones de escritorio. Si todavía quiere usarlo, suprima el mensaje de error del compilador escribiendo la línea [**#pragma warning(suppress: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) justo antes de la llamada [**a ID2D1Factory::GetDesktopDpi.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) Aunque no se recomienda, es posible establecer el reconocimiento de PPP predeterminado mediante programación mediante [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext). Una vez que se ha creado una ventana (un HWND) en el proceso, ya no se admite el cambio del modo de reconocimiento de PPP. Si va a establecer el modo de reconocimiento de PPP predeterminado del proceso mediante programación, debe llamar a la API correspondiente antes de que se hayan creado los HWND. Para obtener información, [vea Establecer el reconocimiento de PPP predeterminado para un proceso](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).

## <a name="resizing-the-render-target"></a>Redimensionar el destino de representación

Si cambia el tamaño de la ventana, debe cambiar el tamaño del destino de representación para que coincida. En la mayoría de los casos, también deberá actualizar el diseño y volver a dibujar la ventana. En el código siguiente se muestran estos pasos.


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



La [**función GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) obtiene el nuevo tamaño del área de cliente, en píxeles físicos (no EN DIP). El [**método ID2D1HwndRenderTarget::Resize**](../direct2d/id2d1hwndrendertarget-resize.md) actualiza el tamaño del destino de representación, también especificado en píxeles. La [**función InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) fuerza un repintado agregando todo el área de cliente a la región de actualización de la ventana. (Vea [Pintar la ventana](painting-the-window.md), en el módulo 1).

A medida que la ventana crece o se reduce, normalmente tendrá que volver a calcular la posición de los objetos que dibuje. Por ejemplo, en el programa de círculo, se deben actualizar el radio y el punto central:


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



El [**método ID2D1RenderTarget::GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) devuelve el tamaño del destino de representación en DIP (no píxeles), que es la unidad adecuada para calcular el diseño. Hay un método estrechamente relacionado, [**ID2D1RenderTarget::GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), que devuelve el tamaño en píxeles físicos. Para un **destino de representación HWND,** este valor coincide con el tamaño devuelto por [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect). Pero recuerde que el dibujo se realiza en DIP, no en píxeles.

## <a name="next"></a>Siguientes

[Uso de color en Direct2D](using-color-in-direct2d.md)

 

 
