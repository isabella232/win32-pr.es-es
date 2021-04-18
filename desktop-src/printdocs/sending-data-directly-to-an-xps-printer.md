---
description: En este tema se describe cómo enviar datos de control de impresora directamente a las impresoras que usan controladores de impresora XPSDrv.
ms.assetid: 7e98e08a-d572-451d-befb-18fc86f0e505
title: 'Cómo: enviar datos directamente a una impresora XPS'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78a8c36d6862860862059f9bbcc8db25e171b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720520"
---
# <a name="how-to-send-data-directly-to-an-xps-printer"></a><span data-ttu-id="80f71-103">Cómo: enviar datos directamente a una impresora XPS</span><span class="sxs-lookup"><span data-stu-id="80f71-103">How To: Send Data Directly to an XPS Printer</span></span>

<span data-ttu-id="80f71-104">En este tema se describe cómo enviar datos de control de impresora directamente a las impresoras que usan controladores de impresora XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="80f71-104">This topic describes how to send printer control data directly to printers that use XPSDrv printer drivers.</span></span>

<span data-ttu-id="80f71-105">En los pasos siguientes se describe cómo enviar datos directamente a una impresora.</span><span class="sxs-lookup"><span data-stu-id="80f71-105">The following steps describe how to send data directly to a printer.</span></span> <span data-ttu-id="80f71-106">Estos pasos también se ilustran en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="80f71-106">These steps are also illustrated in the code example that follows.</span></span>

1.  <span data-ttu-id="80f71-107">Llame a [**OpenPrinter**](openprinter.md) para obtener un identificador de la impresora.</span><span class="sxs-lookup"><span data-stu-id="80f71-107">Call [**OpenPrinter**](openprinter.md) to get a handle to the printer.</span></span>
2.  <span data-ttu-id="80f71-108">Inicialice una estructura [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) con los datos de la impresora.</span><span class="sxs-lookup"><span data-stu-id="80f71-108">Initialize a [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) structure with the printer data.</span></span>
3.  <span data-ttu-id="80f71-109">Llame a [**StartDocPrinter**](startdocprinter.md) para indicar que la aplicación va a enviar datos de documento a la impresora.</span><span class="sxs-lookup"><span data-stu-id="80f71-109">Call [**StartDocPrinter**](startdocprinter.md) to indicate that the application will be sending document data to the printer.</span></span>
4.  <span data-ttu-id="80f71-110">Llame a [**WritePrinter**](writeprinter.md) para enviar los datos.</span><span class="sxs-lookup"><span data-stu-id="80f71-110">Call [**WritePrinter**](writeprinter.md) to send the data.</span></span>
5.  <span data-ttu-id="80f71-111">Llame a [**EndDocPrinter**](enddocprinter.md) para indicar que se han enviado todos los datos de este documento.</span><span class="sxs-lookup"><span data-stu-id="80f71-111">Call [**EndDocPrinter**](enddocprinter.md) to indicate that all data for this document has been sent.</span></span>
6.  <span data-ttu-id="80f71-112">Llame a [**ClosePrinter**](closeprinter.md) para liberar los recursos.</span><span class="sxs-lookup"><span data-stu-id="80f71-112">Call [**ClosePrinter**](closeprinter.md) to release the resources.</span></span>

<span data-ttu-id="80f71-113">Enviar datos de control de impresora directamente a las impresoras que usan controladores de impresora XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="80f71-113">Send printer control data directly to printers that use XPSDrv printer drivers.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="80f71-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80f71-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80f71-115">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="80f71-115">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="80f71-116">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="80f71-116">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="80f71-117">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="80f71-117">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="80f71-118">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="80f71-118">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="80f71-119">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="80f71-119">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="80f71-120">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="80f71-120">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="80f71-121">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="80f71-121">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 
