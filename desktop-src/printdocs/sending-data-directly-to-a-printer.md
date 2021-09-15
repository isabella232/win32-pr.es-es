---
description: El ejemplo de código que aparece más adelante en este tema muestra cómo enviar datos de control de impresora directamente a impresoras que usan controladores de impresora basados en GDI.
ms.assetid: 321f2333-d88e-4042-b9b1-0d918b3209d4
title: 'Cómo: Enviar datos directamente a una impresora GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1968b435068a62ce7a7d379a66c1500d04d8936a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568608"
---
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a>Cómo: Enviar datos directamente a una impresora GDI

El ejemplo de código que aparece más adelante en este tema muestra cómo enviar datos de control de impresora directamente a impresoras que usan controladores de impresora basados en GDI.

En los pasos siguientes se describe cómo enviar datos directamente a una impresora. Estos pasos también se ilustran en el ejemplo de código siguiente.

1.  Llame [**a OpenPrinter**](openprinter.md) para obtener un identificador para la impresora.
2.  Inicialice [**una estructura DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) con los datos de la impresora.
3.  Llame [**a StartDocPrinter**](startdocprinter.md) para indicar que la aplicación enviará datos del documento a la impresora.
4.  Llame [**a StartPagePrinter**](startpageprinter.md) para indicar que la aplicación enviará una nueva página a la impresora.
5.  Llame [**a WritePrinter**](writeprinter.md) para enviar los datos.
6.  Llame [**a EndPagePrinter**](endpageprinter.md) para indicar que se han enviado todos los datos de la página actual.
7.  Llame [**a EndDocPrinter**](enddocprinter.md) para indicar que se han enviado todos los datos de este documento.
8.  Llame [**a ClosePrinter**](closeprinter.md) para liberar los recursos.

Enviar datos de control de impresora directamente a impresoras que usan controladores de impresora basados en GDI.


```C++
// 
// RawDataToPrinter - sends binary data directly to a printer 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToPrinter(LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1 DocInfo;
    DWORD      dwJob = 0L;
    DWORD      dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter( szPrinterName, &hPrinter, NULL );
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;
        DocInfo.pDatatype = (LPTSTR)_T("RAW");

        // Inform the spooler the document is beginning. 
        dwJob = StartDocPrinter( hPrinter, 1, (LPBYTE)&DocInfo );
        if (dwJob > 0) {
            // Start a page. 
            bStatus = StartPagePrinter( hPrinter );
            if (bStatus) {
                // Send the data to the printer. 
                bStatus = WritePrinter( hPrinter, lpData, dwCount, &dwBytesWritten);
                EndPagePrinter (hPrinter);
            }
            // Inform the spooler that the document is ending. 
            EndDocPrinter( hPrinter );
        }
        // Close the printer handle. 
        ClosePrinter( hPrinter );
    }
    // Check to see if correct number of bytes were written. 
    if (!bStatus || (dwBytesWritten != dwCount)) {
        bStatus = FALSE;
    } else {
        bStatus = TRUE;
    }
    return bStatus;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 
