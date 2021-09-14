---
title: Usar estilos visuales con controles personalizados y Owner-Drawn personalizados
description: En este tema se describe cómo usar la API de estilos visuales para aplicar estilos visuales a controles personalizados o controles dibujados por el propietario.
ms.assetid: 8b06f9ce-702c-48f8-8cf3-2718a09b8d77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7025bdf7c589649ac62bed7a4ea4f55c418940
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165274"
---
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a>Usar estilos visuales con controles personalizados y Owner-Drawn personalizados

En este tema se describe cómo usar la API de estilos visuales para aplicar estilos visuales a controles personalizados o controles dibujados por el propietario.

-   [Dibujar controles con estilos visuales](#drawing-controls-with-visual-styles)
-   [Respuesta a los cambios de tema](#responding-to-theme-changes)
-   [Temas relacionados](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a>Dibujar controles con estilos visuales

Los estilos visuales son compatibles con ComCtrl32.dll versión 6 y posteriores. Si la aplicación está configurada para usar ComCtrl32.dll versión 6 y posteriores, y si esa versión está disponible en el sistema, los estilos visuales actuales se aplican automáticamente ComCtrl32.dll todos los controles comunes de la aplicación. Sin embargo, los estilos visuales actuales no se aplican automáticamente a controles personalizados o controles dibujados por el propietario. La aplicación debe incluir código que comprueba si los estilos visuales están disponibles y, si es así, usa la API de estilos visuales para aplicar los estilos visuales seleccionados actualmente a los controles personalizados y dibujados por el propietario.

Para comprobar si los estilos visuales están disponibles, llame a [**la función IsAppThemed.**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) Si los estilos visuales no están disponibles, use código de reserva para dibujar el control.

Si hay estilos visuales disponibles, puede usar funciones de estilos visuales como [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) para representar el control. Tenga en [**cuenta que DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) le permite personalizar la apariencia del texto, conservando algunas propiedades de la fuente de tema mientras modifica otras.

**Para dibujar un control en el estilo visual actual**

1.  Llame [**a OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), pasando el *hwnd* del control al que desea aplicar estilos visuales y una lista de clases que describe el tipo del control. Las clases se definen en Vssym32.h. **OpenThemeData** devuelve un identificador HTHEME, pero si el administrador de estilos visuales está deshabilitado o el estilo visual actual no proporciona información específica para un control determinado, la función devuelve **NULL.** Si el valor devuelto es **NULL,** use funciones de dibujo de estilos no visuales.
2.  Para dibujar el fondo del control, llame [**a DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) o [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).
3.  Para determinar la ubicación del rectángulo de contenido, llame a [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).
4.  Para representar texto, use [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) o [**DrawThemeTextEx,**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex)basándose en las coordenadas del rectángulo devuelto por [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect). Estas funciones pueden representar texto en la fuente del tema para una parte y un estado de control especificados, o bien en la fuente seleccionada actualmente en el contexto del dispositivo (DC).
5.  Cuando el control recibe un [**mensaje WM \_ DESTROY,**](/windows/desktop/winmsg/wm-destroy) llame a [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) para liberar el identificador de tema que se devolvió cuando llamó a [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).

En el código de ejemplo siguiente se muestra una manera de dibujar un control de botón en el estilo visual actual.


```C++
HTHEME hTheme = NULL;

hTheme = OpenThemeData(hwndButton, L"Button");
// ...
DrawMyControl(hDC, hwndButton, hTheme, iState);
// ...
if (hTheme)
{
    CloseThemeData(hTheme);
}


void DrawMyControl(HDC hDC, HWND hwndButton, HTHEME hTheme, int iState)
{
    RECT rc, rcContent;
    TCHAR szButtonText[255];
    HRESULT hr;
    size_t cch;

    GetWindowRect(hwndButton, &rc);
    GetWindowText(hwndButton, szButtonText,
                  (sizeof(szButtonText) / sizeof(szButtonText[0])+1));
    hr = StringCchLength(szButtonText,
         (sizeof(szButtonText) / sizeof(szButtonText[0])), &cch);
    if (hTheme)
    {
        hr = DrawThemeBackground(hTheme, hDC, BP_PUSHBUTTON, iState, &rc, 0);
        if (SUCCEEDED(hr))
        {
            hr = GetThemeBackgroundContentRect(hTheme, hDC, BP_PUSHBUTTON, 
                    iState, &rc, &rcContent);
        }

        if (SUCCEEDED(hr))
        {
            hr = DrawThemeText(hTheme, hDC, BP_PUSHBUTTON, iState, 
                    szButtonText, cch,
                    DT_CENTER | DT_VCENTER | DT_SINGLELINE,
                    0, &rcContent);
        }

    }
    else
    {
        // Draw the control without using visual styles.
    }
}
```





El código de ejemplo siguiente está en el [**controlador de mensajes WM \_ PAINT**](/windows/desktop/gdi/wm-paint) para un control de botón con subclases. El texto del control se dibuja en la fuente de estilos visuales, pero el color está definido por la aplicación en función del estado del control.


```C++
// textColor is a COLORREF whose value has been set according to whether the button is "hot".
// paint is the PAINTSTRUCT whose members are filled in by BeginPaint.
HTHEME theme = OpenThemeData(hWnd, L"button");
if (theme)
{
    DTTOPTS opts = { 0 };
    opts.dwSize = sizeof(opts);
    opts.crText = textColor;
    opts.dwFlags |= DTT_TEXTCOLOR;
    WCHAR caption[255];
    size_t cch;
    GetWindowText(hWnd, caption, 255);
    StringCchLength(caption, 255, &cch);
    DrawThemeTextEx(theme, paint.hdc, BP_PUSHBUTTON, CBS_UNCHECKEDNORMAL, 
        caption, cch, DT_CENTER | DT_VCENTER | DT_SINGLELINE, 
        &paint.rcPaint, &opts);
    CloseThemeData(theme);
}
else
{
    // Draw the control without using visual styles.
}
```



Puede usar elementos de otros controles y representar cada elemento por separado. Por ejemplo, para un control de calendario que consta de una cuadrícula, puede tratar cada cuadrado formado por la cuadrícula como un botón de barra de herramientas, obteniendo el identificador de tema como se muestra a continuación:


```C++
OpenThemeData(hwnd, L"Toolbar");
```



Puede mezclar y buscar coincidencias con elementos de control llamando a [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) varias veces para un control determinado y usando el identificador de tema adecuado para dibujar diferentes partes. Sin embargo, en algunos estilos visuales, es posible que algunas partes no sean compatibles con otras partes.

Otro enfoque para representar controles en el estilo visual activo es usar los colores del sistema. Por ejemplo, puede usar colores del sistema para establecer el color del texto al llamar a la [**función DrawThemeTextEx.**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) La mayoría de los colores del sistema se establecen cuando se aplica un archivo de estilo visual.

## <a name="responding-to-theme-changes"></a>Respuesta a los cambios de tema

Cuando el control recibe un [**mensaje \_ WM THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) y mantiene un identificador global para el tema, debe hacer lo siguiente:

-   Llame [**a CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) para cerrar el identificador de tema existente.
-   Llame [**a OpenThemeData para**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) obtener el identificador del tema al estilo visual recién cargado.

En el ejemplo siguiente se muestran las dos llamadas.


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar los estilos visuales](cookbook-overview.md)
</dt> <dt>

[Estilos visuales](themes-overview.md)
</dt> </dl>

 

 