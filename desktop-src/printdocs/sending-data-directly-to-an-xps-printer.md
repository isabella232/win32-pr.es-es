---
description: En este tema se describe cómo enviar datos de control de impresora directamente a impresoras que usan controladores de impresora XPSDrv.
ms.assetid: 7e98e08a-d572-451d-befb-18fc86f0e505
title: 'Cómo: Enviar datos directamente a una impresora XPS'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65fba87578f9257290123b737f2d1d8c3e48f57e6a628110a20a232ddb290ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470157"
---
# <a name="how-to-send-data-directly-to-an-xps-printer"></a>Cómo: Enviar datos directamente a una impresora XPS

En este tema se describe cómo enviar datos de control de impresora directamente a impresoras que usan controladores de impresora XPSDrv.

En los pasos siguientes se describe cómo enviar datos directamente a una impresora. Estos pasos también se muestran en el ejemplo de código siguiente.

1.  Llame [**a OpenPrinter**](openprinter.md) para obtener un identificador para la impresora.
2.  Inicialice [**una estructura DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) con los datos de la impresora.
3.  Llame [**a StartDocPrinter**](startdocprinter.md) para indicar que la aplicación enviará datos del documento a la impresora.
4.  Llame [**a WritePrinter**](writeprinter.md) para enviar los datos.
5.  Llame [**a EndDocPrinter**](enddocprinter.md) para indicar que se han enviado todos los datos de este documento.
6.  Llame [**a ClosePrinter**](closeprinter.md) para liberar los recursos.

Envíe datos de control de impresora directamente a las impresoras que usan controladores de impresora XPSDrv.


```C++
// 
//  RawDataToXpsPrinter - sends binary data directly to a printer 
//          with an XPSDrv Printer Driver 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToXpsPrinter (LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1       DocInfo;
    DWORD    dwPrtJob = 0L;
    DWORD    dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter (szPrinterName, &hPrinter, NULL);
    
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;

        // Enter the datatype of this buffer.
        //  Use "XPS_PASS" when the data buffer should bypass the 
        //    print filter pipeline of the XPSDrv printer driver. 
        //    This datatype would be used to send the buffer directly 
        //    to the printer, such as when sending print head alignment 
        //    commands. Normally, a data buffer would be sent as the
        //    "RAW" datatype.
        //
        DocInfo.pDatatype = (LPTSTR)_T("XPS_PASS");

        dwPrtJob = StartDocPrinter (
                        hPrinter,
                        1,
                        (LPBYTE)&DocInfo);

        if (dwPrtJob > 0) {
                // Send the data to the printer. 
                bStatus = WritePrinter (
                hPrinter,
                lpData,
                dwCount,
                &dwBytesWritten);
        }
        
        EndDocPrinter (hPrinter);

        // Close the printer handle. 
        bStatus = ClosePrinter(hPrinter);
    }
    
    if (!bStatus || (dwCount != dwBytesWritten)) {
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

 

 
