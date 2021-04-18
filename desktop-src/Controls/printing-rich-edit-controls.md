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
# <a name="how-to-print-the-contents-of-rich-edit-controls"></a>Cómo imprimir el contenido de los controles Rich Edit

Esta sección contiene información sobre cómo imprimir el contenido de los controles Rich Edit.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="use-print-preview"></a>Usar vista previa de impresión

Para dar formato al texto de un control Rich Edit tal como aparecerá en un dispositivo de destino (normalmente la página impresa), envíe el mensaje [**\_ SETTARGETDEVICE em**](em-settargetdevice.md) , pasando el identificador a un contexto de dispositivo (HDC) del dispositivo de destino y el ancho de línea deseado. Normalmente obtendrá el ancho de línea llamando a [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) para la HDC de destino.

### <a name="format-print-for-a-specific-device"></a>Formato de impresión para un dispositivo específico

Para dar formato a parte del contenido de un control Rich Edit para un dispositivo específico, envíe el mensaje [**\_ FORMATRANGE em**](em-formatrange.md) . La estructura [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) que se usa con este mensaje especifica el intervalo de texto al que se va a dar formato, así como la HDC para el dispositivo de destino. Opcionalmente, este mensaje también envía el texto a la impresora.

### <a name="use-banding"></a>Usar bandas

El uso de bandas es el proceso por el que se genera una sola página de salida mediante uno o varios rectángulos o bandas independientes. Cuando todas las bandas se colocan en la página, se obtiene una imagen completa. Este enfoque suele usarse en impresoras de tramas que no tienen suficiente memoria o capacidad de imagen de una página completa al mismo tiempo.

Para implementar el uso de bandas, use el mensaje [**\_ DISPLAYBAND em**](em-displayband.md) para enviar al dispositivo partes sucesivas del contenido del control Rich Edit. Este mensaje imprime en el dispositivo que se especificó en una llamada anterior a [**em \_ FORMATRANGE**](em-formatrange.md). Por supuesto, el parámetro *wParam* del mensaje **em \_ FORMATRANGE** debe ser cero, por lo que el mensaje no inicia la impresión.

## <a name="printrtf-code-example"></a>Ejemplo de código PrintRTF

En el ejemplo de código siguiente se imprime el contenido de un control Rich Edit en la impresora especificada.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 