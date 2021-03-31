---
title: Cómo procesar la notificación de DTN_FORMATQUERY
description: En este tema se muestra cómo procesar una notificación de consulta de formato enviada por el control de fecha y hora (DTP).
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e8de1e1a80d04f9a7f9e9d0cfcda198118e67c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995766"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a><span data-ttu-id="ae7b0-103">Cómo procesar la notificación de DTN \_ FORMATQUERY</span><span class="sxs-lookup"><span data-stu-id="ae7b0-103">How to Process the DTN\_FORMATQUERY Notification</span></span>

<span data-ttu-id="ae7b0-104">En este tema se muestra cómo procesar una notificación de consulta de formato enviada por el control de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="ae7b0-104">This topic demonstrates how to process a Format Query notification that is sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ae7b0-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="ae7b0-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ae7b0-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="ae7b0-106">Technologies</span></span>

-   [<span data-ttu-id="ae7b0-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="ae7b0-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ae7b0-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ae7b0-108">Prerequisites</span></span>

-   <span data-ttu-id="ae7b0-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="ae7b0-109">C/C++</span></span>
-   <span data-ttu-id="ae7b0-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="ae7b0-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ae7b0-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="ae7b0-111">Instructions</span></span>


<span data-ttu-id="ae7b0-112">Un control de DTP envía un código de notificación de [DTN \_ FORMATQUERY](dtn-formatquery.md) para solicitar información sobre el tamaño máximo posible de un campo de devolución de llamada en el control.</span><span class="sxs-lookup"><span data-stu-id="ae7b0-112">A DTP control sends a [DTN\_FORMATQUERY](dtn-formatquery.md) notification code to request information about the maximum possible size of a callback field within the control.</span></span> <span data-ttu-id="ae7b0-113">La aplicación debe controlar este mensaje para asegurarse de que todos los campos se muestran correctamente.</span><span class="sxs-lookup"><span data-stu-id="ae7b0-113">Your application must handle this message to ensure that all fields are displayed properly.</span></span>

<span data-ttu-id="ae7b0-114">El siguiente ejemplo de código C++ es una función definida por la aplicación que procesa el código de notificación de [DTN \_ FORMATQUERY](dtn-formatquery.md) calculando el ancho de la cadena más ancha posible para un campo de devolución de llamada determinado.</span><span class="sxs-lookup"><span data-stu-id="ae7b0-114">The following C++ code example is an application-defined function that processes the [DTN\_FORMATQUERY](dtn-formatquery.md) notification code by calculating the width of the widest possible string for a given callback field.</span></span>

<span data-ttu-id="ae7b0-115">**Advertencia de seguridad:** El uso incorrecto de **lstrcmp** puede poner en peligro la seguridad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ae7b0-115">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="ae7b0-116">Por ejemplo, antes de llamar a **lstrcmp** en el ejemplo de código siguiente, debe asegurarse de que las dos cadenas terminan en NULL.</span><span class="sxs-lookup"><span data-stu-id="ae7b0-116">For example, before calling **lstrcmp** in the following code example you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="ae7b0-117">Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="ae7b0-117">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



```C++
//  DoFormatQuery processes DTN_FORMATQUERY messages to ensure that the
//  DTP control displays callback fields properly.
//

void WINAPI DoFormatQuery(
 HWND hwndDP, 
 LPNMDATETIMEFORMATQUERY lpDTFQuery)
{
    HDC hdc;
    HFONT hFont, hOrigFont;

    //  Prepare the device context for GetTextExtentPoint32 call.
    hdc = GetDC(hwndDP);

    hFont = (HFONT) SendMessage(hwndDP, WM_GETFONT, 0L, 0L); 

    if(!hFont)
        hFont = (HFONT)GetStockObject(DEFAULT_GUI_FONT);

    hOrigFont = (HFONT) SelectObject(hdc, hFont);

    // Check to see if this is the callback segment desired. If so,
    // use the longest text segment to determine the maximum 
    // width of the callback field, and then place the information into 
    // the NMDATETIMEFORMATQUERY structure.
    if(!lstrcmp(L"XX",lpDTFQuery->pszFormat))
        GetTextExtentPoint32 (hdc,
                          L"366",  // widest date string
                          3,
                          &lpDTFQuery->szMax);

    // Reset the font in the device context; then release the context.
    SelectObject(hdc,hOrigFont);
    ReleaseDC(hwndDP, hdc);
}
```



## <a name="related-topics"></a><span data-ttu-id="ae7b0-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae7b0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae7b0-119">Usar controles de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="ae7b0-119">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="ae7b0-120">Referencia de control de selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="ae7b0-120">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ae7b0-121">Selector de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="ae7b0-121">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




