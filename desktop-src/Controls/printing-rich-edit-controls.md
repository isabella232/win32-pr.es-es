---
title: Cómo imprimir el contenido de los controles Rich Edit
description: Esta sección contiene información sobre cómo imprimir el contenido de los controles Rich Edit.
ms.assetid: d61e2e11-d848-43fc-9622-b3b2032bda48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a304e5c09b5f8ea934c90873c3d915179295964e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656429"
---
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a><span data-ttu-id="446ff-103">Cómo imprimir el contenido de los controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="446ff-103">How to Print the Contents of Rich Edit Controls</span></span>

<span data-ttu-id="446ff-104">Esta sección contiene información sobre cómo imprimir el contenido de los controles Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="446ff-104">This section contains information about how to print the contents of rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="446ff-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="446ff-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="446ff-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="446ff-106">Technologies</span></span>

-   [<span data-ttu-id="446ff-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="446ff-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="446ff-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="446ff-108">Prerequisites</span></span>

-   <span data-ttu-id="446ff-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="446ff-109">C/C++</span></span>
-   <span data-ttu-id="446ff-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="446ff-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="446ff-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="446ff-111">Instructions</span></span>

### <a name="use-print-preview"></a><span data-ttu-id="446ff-112">Usar vista previa de impresión</span><span class="sxs-lookup"><span data-stu-id="446ff-112">Use Print Preview</span></span>

<span data-ttu-id="446ff-113">Para dar formato al texto de un control Rich Edit tal como aparecerá en un dispositivo de destino (normalmente la página impresa), envíe el mensaje [**\_ SETTARGETDEVICE em**](em-settargetdevice.md) , pasando el identificador a un contexto de dispositivo (HDC) del dispositivo de destino y el ancho de línea deseado.</span><span class="sxs-lookup"><span data-stu-id="446ff-113">To format text in a rich edit control as it will appear on a target device (usually the printed page), send the [**EM\_SETTARGETDEVICE**](em-settargetdevice.md) message, passing in the handle to a device context (HDC) of the target device and the desired line width.</span></span> <span data-ttu-id="446ff-114">Normalmente obtendrá el ancho de línea llamando a [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) para la HDC de destino.</span><span class="sxs-lookup"><span data-stu-id="446ff-114">Usually you will obtain the line width by calling [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) for the target HDC.</span></span>

### <a name="format-print-for-a-specific-device"></a><span data-ttu-id="446ff-115">Formato de impresión para un dispositivo específico</span><span class="sxs-lookup"><span data-stu-id="446ff-115">Format Print for a Specific Device</span></span>

<span data-ttu-id="446ff-116">Para dar formato a parte del contenido de un control Rich Edit para un dispositivo específico, envíe el mensaje [**\_ FORMATRANGE em**](em-formatrange.md) .</span><span class="sxs-lookup"><span data-stu-id="446ff-116">To format part of a rich edit control's contents for a specific device, send the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span> <span data-ttu-id="446ff-117">La estructura [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) que se usa con este mensaje especifica el intervalo de texto al que se va a dar formato, así como la HDC para el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="446ff-117">The [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure that is used with this message specifies the range of text to format as well as the HDC for the target device.</span></span> <span data-ttu-id="446ff-118">Opcionalmente, este mensaje también envía el texto a la impresora.</span><span class="sxs-lookup"><span data-stu-id="446ff-118">Optionally, this message also sends the text to the printer.</span></span>

### <a name="use-banding"></a><span data-ttu-id="446ff-119">Usar bandas</span><span class="sxs-lookup"><span data-stu-id="446ff-119">Use Banding</span></span>

<span data-ttu-id="446ff-120">El uso de bandas es el proceso por el que se genera una sola página de salida mediante uno o varios rectángulos o bandas independientes.</span><span class="sxs-lookup"><span data-stu-id="446ff-120">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="446ff-121">Cuando todas las bandas se colocan en la página, se obtiene una imagen completa.</span><span class="sxs-lookup"><span data-stu-id="446ff-121">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="446ff-122">Este enfoque suele usarse en impresoras de tramas que no tienen suficiente memoria o capacidad de imagen de una página completa al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="446ff-122">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span>

<span data-ttu-id="446ff-123">Para implementar el uso de bandas, use el mensaje [**\_ DISPLAYBAND em**](em-displayband.md) para enviar al dispositivo partes sucesivas del contenido del control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="446ff-123">To implement banding, use the [**EM\_DISPLAYBAND**](em-displayband.md) message to send successive portions of the rich edit control's content to the device.</span></span> <span data-ttu-id="446ff-124">Este mensaje imprime en el dispositivo que se especificó en una llamada anterior a [**em \_ FORMATRANGE**](em-formatrange.md).</span><span class="sxs-lookup"><span data-stu-id="446ff-124">This message prints to the device that was specified in a previous call to [**EM\_FORMATRANGE**](em-formatrange.md).</span></span> <span data-ttu-id="446ff-125">Por supuesto, el parámetro *wParam* del mensaje **em \_ FORMATRANGE** debe ser cero, por lo que el mensaje no inicia la impresión.</span><span class="sxs-lookup"><span data-stu-id="446ff-125">Of course, the *wParam* parameter of the **EM\_FORMATRANGE** message should be zero, so that printing is not initiated by that message.</span></span>

## <a name="printrtf-code-example"></a><span data-ttu-id="446ff-126">Ejemplo de código PrintRTF</span><span class="sxs-lookup"><span data-stu-id="446ff-126">PrintRTF Code Example</span></span>

<span data-ttu-id="446ff-127">En el ejemplo de código siguiente se imprime el contenido de un control Rich Edit en la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="446ff-127">The following example code prints the contents of a rich edit control to the specified printer.</span></span>


```C++
// hwnd is the HWND of the rich edit control.
// hdc is the HDC of the printer. This value can be obtained for the 
// default printer as follows:
//
//     PRINTDLG pd = { sizeof(pd) };
//     pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
//
//     if (PrintDlg(&pd))
//     {
//        HDC hdc = pd.hDC;
//        ...
//     }

BOOL PrintRTF(HWND hwnd, HDC hdc)
{
    DOCINFO di = { sizeof(di) };
    
    if (!StartDoc(hdc, &di))
    {
        return FALSE;
    }

    int cxPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETX);
    int cyPhysOffset = GetDeviceCaps(hdc, PHYSICALOFFSETY);
    
    int cxPhys = GetDeviceCaps(hdc, PHYSICALWIDTH);
    int cyPhys = GetDeviceCaps(hdc, PHYSICALHEIGHT);

    // Create "print preview". 
    SendMessage(hwnd, EM_SETTARGETDEVICE, (WPARAM)hdc, cxPhys/2);

    FORMATRANGE fr;

    fr.hdc       = hdc;
    fr.hdcTarget = hdc;

    // Set page rect to physical page size in twips.
    fr.rcPage.top    = 0;  
    fr.rcPage.left   = 0;  
    fr.rcPage.right  = MulDiv(cxPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSX));  
    fr.rcPage.bottom = MulDiv(cyPhys, 1440, GetDeviceCaps(hDC, LOGPIXELSY)); 

    // Set the rendering rectangle to the pintable area of the page.
    fr.rc.left   = cxPhysOffset;
    fr.rc.right  = cxPhysOffset + cxPhys;
    fr.rc.top    = cyPhysOffset;
    fr.rc.bottom = cyPhysOffset + cyPhys;

    SendMessage(hwnd, EM_SETSEL, 0, (LPARAM)-1);          // Select the entire contents.
    SendMessage(hwnd, EM_EXGETSEL, 0, (LPARAM)&fr.chrg);  // Get the selection into a CHARRANGE.

    BOOL fSuccess = TRUE;

    // Use GDI to print successive pages.
    while (fr.chrg.cpMin < fr.chrg.cpMax && fSuccess) 
    {
        fSuccess = StartPage(hdc) > 0;
        
        if (!fSuccess) break;
        
        int cpMin = SendMessage(hwnd, EM_FORMATRANGE, TRUE, (LPARAM)&fr);
        
        if (cpMin <= fr.chrg.cpMin) 
        {
            fSuccess = FALSE;
            break;
        }
        
        fr.chrg.cpMin = cpMin;
        fSuccess = EndPage(hdc) > 0;
    }
    
    SendMessage(hwnd, EM_FORMATRANGE, FALSE, 0);
    
    if (fSuccess)
    {
        EndDoc(hdc);
    } 
    
    else 
    
    {
        AbortDoc(hdc);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="446ff-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="446ff-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="446ff-129">Usar controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="446ff-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="446ff-130">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="446ff-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 