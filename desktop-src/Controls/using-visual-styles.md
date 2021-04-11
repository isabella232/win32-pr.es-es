---
title: Usar estilos visuales con controles personalizados y Owner-Drawn
description: En este tema se describe cómo usar la API de estilos visuales para aplicar estilos visuales a controles personalizados o controles dibujados por el propietario.
ms.assetid: 8b06f9ce-702c-48f8-8cf3-2718a09b8d77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7025bdf7c589649ac62bed7a4ea4f55c418940
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149671"
---
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a><span data-ttu-id="92af0-103">Usar estilos visuales con controles personalizados y Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="92af0-103">Using Visual Styles with Custom and Owner-Drawn Controls</span></span>

<span data-ttu-id="92af0-104">En este tema se describe cómo usar la API de estilos visuales para aplicar estilos visuales a controles personalizados o controles dibujados por el propietario.</span><span class="sxs-lookup"><span data-stu-id="92af0-104">This topic describes how to use the visual styles API to apply visual styles to custom controls or owner-drawn controls.</span></span>

-   [<span data-ttu-id="92af0-105">Dibujar controles con estilos visuales</span><span class="sxs-lookup"><span data-stu-id="92af0-105">Drawing Controls with Visual Styles</span></span>](#drawing-controls-with-visual-styles)
-   [<span data-ttu-id="92af0-106">Responder a los cambios de tema</span><span class="sxs-lookup"><span data-stu-id="92af0-106">Responding to Theme Changes</span></span>](#responding-to-theme-changes)
-   [<span data-ttu-id="92af0-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92af0-107">Related topics</span></span>](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a><span data-ttu-id="92af0-108">Dibujar controles con estilos visuales</span><span class="sxs-lookup"><span data-stu-id="92af0-108">Drawing Controls with Visual Styles</span></span>

<span data-ttu-id="92af0-109">ComCtrl32.dll versión 6 y versiones posteriores admiten los estilos visuales.</span><span class="sxs-lookup"><span data-stu-id="92af0-109">Visual styles are supported by ComCtrl32.dll version 6 and later.</span></span> <span data-ttu-id="92af0-110">Si la aplicación está configurada para usar ComCtrl32.dll versión 6 y versiones posteriores, y si esa versión está disponible en el sistema, los estilos visuales actuales se aplican automáticamente a todos los controles comunes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="92af0-110">If your application is configured to use ComCtrl32.dll version 6 and later, and if that version is available on the system, the current visual styles are automatically applied to all common controls in your application.</span></span> <span data-ttu-id="92af0-111">Sin embargo, los estilos visuales actuales no se aplican automáticamente a controles personalizados ni a controles dibujados por el propietario.</span><span class="sxs-lookup"><span data-stu-id="92af0-111">However, the current visual styles are not automatically applied to custom controls or owner-drawn controls.</span></span> <span data-ttu-id="92af0-112">La aplicación debe incluir código que compruebe si los estilos visuales están disponibles y, si es así, usa la API de estilos visuales para aplicar los estilos visuales seleccionados actualmente a los controles personalizados y dibujados por el propietario.</span><span class="sxs-lookup"><span data-stu-id="92af0-112">Your application must include code that checks whether visual styles are available and, if so, uses the visual styles API to apply the currently selected visual styles to your custom and owner-drawn controls.</span></span>

<span data-ttu-id="92af0-113">Para comprobar si los estilos visuales están disponibles, llame a la función [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) .</span><span class="sxs-lookup"><span data-stu-id="92af0-113">To check whether visual styles are available, call the [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) function.</span></span> <span data-ttu-id="92af0-114">Si los estilos visuales no están disponibles, use el código de reserva para dibujar el control.</span><span class="sxs-lookup"><span data-stu-id="92af0-114">If visual styles are not available, use fallback code to draw the control.</span></span>

<span data-ttu-id="92af0-115">Si los estilos visuales están disponibles, puede usar funciones de estilos visuales, como [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) , para representar el control.</span><span class="sxs-lookup"><span data-stu-id="92af0-115">If visual styles are available, you can use visual-styles functions such as [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) to render your control.</span></span> <span data-ttu-id="92af0-116">Tenga en cuenta que [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) le permite personalizar la apariencia del texto, conservando algunas propiedades de la fuente del tema mientras modifica otras.</span><span class="sxs-lookup"><span data-stu-id="92af0-116">Note that [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) enables you to customize the appearance of text, retaining some properties of the theme font while modifying others.</span></span>

<span data-ttu-id="92af0-117">**Para dibujar un control en el estilo visual actual**</span><span class="sxs-lookup"><span data-stu-id="92af0-117">**To draw a control in the current visual style**</span></span>

1.  <span data-ttu-id="92af0-118">Llame a [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), pasando el *hWnd* del control al que desea aplicar los estilos visuales y una lista de clases que describa el tipo del control.</span><span class="sxs-lookup"><span data-stu-id="92af0-118">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), passing the *hwnd* of the control you want to apply visual styles to and a class list that describes the control's type.</span></span> <span data-ttu-id="92af0-119">Las clases se definen en Vssym32. h.</span><span class="sxs-lookup"><span data-stu-id="92af0-119">The classes are defined in Vssym32.h.</span></span> <span data-ttu-id="92af0-120">**OpenThemeData** devuelve un identificador HTHEME, pero si el administrador de estilos visuales está deshabilitado o el estilo visual actual no proporciona información específica para un control determinado, la función devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="92af0-120">**OpenThemeData** returns an HTHEME handle, but if the visual styles manager is disabled or the current visual style does not supply specific information for a given control, the function returns **NULL**.</span></span> <span data-ttu-id="92af0-121">Si el valor devuelto es **null**, use funciones de dibujo que no sean de estilos visuales.</span><span class="sxs-lookup"><span data-stu-id="92af0-121">If the return value is **NULL**, use non-visual-styles drawing functions.</span></span>
2.  <span data-ttu-id="92af0-122">Para dibujar el fondo del control, llame a [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) o [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).</span><span class="sxs-lookup"><span data-stu-id="92af0-122">To draw the control background, call [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) or [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).</span></span>
3.  <span data-ttu-id="92af0-123">Para determinar la ubicación del rectángulo de contenido, llame a [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span><span class="sxs-lookup"><span data-stu-id="92af0-123">To determine the location of the content rectangle, call [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span>
4.  <span data-ttu-id="92af0-124">Para representar texto, use [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) o [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), basando las coordenadas en el rectángulo devuelto por [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span><span class="sxs-lookup"><span data-stu-id="92af0-124">To render text, use either [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) or [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), basing the coordinates on the rectangle returned by [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span> <span data-ttu-id="92af0-125">Estas funciones pueden representar texto en la fuente del tema para una parte de control y estado especificados, o bien en la fuente seleccionada actualmente en el contexto de dispositivo (DC).</span><span class="sxs-lookup"><span data-stu-id="92af0-125">These functions can render text either in the theme's font for a specified control part and state, or in the font currently selected into the device context (DC).</span></span>
5.  <span data-ttu-id="92af0-126">Cuando el control recibe un mensaje de [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) , llame a [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) para liberar el identificador de tema que se devolvió al llamar a [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).</span><span class="sxs-lookup"><span data-stu-id="92af0-126">When your control receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to release the theme handle that was returned when you called [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="92af0-127">En el código de ejemplo siguiente se muestra una manera de dibujar un control de botón en el estilo visual actual.</span><span class="sxs-lookup"><span data-stu-id="92af0-127">The following example code demonstrates one way to draw a button control in the current visual style.</span></span>


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





<span data-ttu-id="92af0-128">El siguiente código de ejemplo se encuentra en el controlador de mensajes de [**\_ Paint de WM**](/windows/desktop/gdi/wm-paint) para un control de botón de subclase.</span><span class="sxs-lookup"><span data-stu-id="92af0-128">The following example code is in the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message handler for a subclassed button control.</span></span> <span data-ttu-id="92af0-129">El texto del control se dibuja en la fuente de estilos visuales, pero el color está definido por la aplicación en función del estado del control.</span><span class="sxs-lookup"><span data-stu-id="92af0-129">The text for the control is drawn in the visual styles font, but the color is application-defined depending on the state of the control.</span></span>


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



<span data-ttu-id="92af0-130">Puede usar elementos de otros controles y representar cada parte por separado.</span><span class="sxs-lookup"><span data-stu-id="92af0-130">You can use parts from other controls and render each part separately.</span></span> <span data-ttu-id="92af0-131">Por ejemplo, para un control de calendario que se compone de una cuadrícula, puede tratar cada cuadrado formado por la cuadrícula como un botón de la barra de herramientas, obteniendo el identificador de tema como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="92af0-131">For example, for a calendar control that consists of a grid, you can treat each square formed by the grid as a toolbar button, by obtaining the theme handle as follows:</span></span>


```C++
OpenThemeData(hwnd, L"Toolbar");
```



<span data-ttu-id="92af0-132">Puede mezclar y hacer coincidir partes de control llamando a [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) varias veces para un control determinado y usando el identificador de tema adecuado para dibujar diferentes partes.</span><span class="sxs-lookup"><span data-stu-id="92af0-132">You can mix and match control parts by calling [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) multiple times for a given control and using the appropriate theme handle to draw different parts.</span></span> <span data-ttu-id="92af0-133">Sin embargo, en algunos estilos visuales, algunas partes podrían no ser compatibles con otras partes.</span><span class="sxs-lookup"><span data-stu-id="92af0-133">In some visual styles, however, certain parts might not be compatible with other parts.</span></span>

<span data-ttu-id="92af0-134">Otro enfoque para representar controles en el estilo visual activo es usar los colores del sistema.</span><span class="sxs-lookup"><span data-stu-id="92af0-134">Another approach to rendering controls in the active visual style is to use the system colors.</span></span> <span data-ttu-id="92af0-135">Por ejemplo, puede usar colores del sistema para establecer el color del texto al llamar a la función [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) .</span><span class="sxs-lookup"><span data-stu-id="92af0-135">For example, you can use system colors to set the text color when calling the [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="92af0-136">La mayoría de los colores del sistema se establecen cuando se aplica un archivo de estilo visual.</span><span class="sxs-lookup"><span data-stu-id="92af0-136">Most system colors are set when a visual style file is applied.</span></span>

## <a name="responding-to-theme-changes"></a><span data-ttu-id="92af0-137">Responder a los cambios de tema</span><span class="sxs-lookup"><span data-stu-id="92af0-137">Responding to Theme Changes</span></span>

<span data-ttu-id="92af0-138">Cuando el control recibe un mensaje de [**\_ THEMECHANGED de WM**](/windows/desktop/winmsg/wm-themechanged) y mantiene un identificador global del tema, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="92af0-138">When your control receives a [**WM\_THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) message and is holding a global handle to the theme, it should do the following:</span></span>

-   <span data-ttu-id="92af0-139">Llame a [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) para cerrar el identificador de tema existente.</span><span class="sxs-lookup"><span data-stu-id="92af0-139">Call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to close the existing theme handle.</span></span>
-   <span data-ttu-id="92af0-140">Llame a [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) para obtener el identificador de tema para el estilo visual recién cargado.</span><span class="sxs-lookup"><span data-stu-id="92af0-140">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) to get the theme handle to the newly loaded visual style.</span></span>

<span data-ttu-id="92af0-141">En el ejemplo siguiente se muestran las dos llamadas a.</span><span class="sxs-lookup"><span data-stu-id="92af0-141">The following example illustrates the two calls.</span></span>


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a><span data-ttu-id="92af0-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92af0-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92af0-143">Habilitar los estilos visuales</span><span class="sxs-lookup"><span data-stu-id="92af0-143">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="92af0-144">Estilos visuales</span><span class="sxs-lookup"><span data-stu-id="92af0-144">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 