---
description: En el ejemplo de código que aparece más adelante en este tema se muestra cómo enviar datos de control de impresora directamente a las impresoras que usan controladores de impresora basados en GDI.
ms.assetid: 321f2333-d88e-4042-b9b1-0d918b3209d4
title: 'Cómo: enviar datos directamente a una impresora GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1968b435068a62ce7a7d379a66c1500d04d8936a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720614"
---
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a><span data-ttu-id="138cc-103">Cómo: enviar datos directamente a una impresora GDI</span><span class="sxs-lookup"><span data-stu-id="138cc-103">How To: Send Data Directly to a GDI Printer</span></span>

<span data-ttu-id="138cc-104">En el ejemplo de código que aparece más adelante en este tema se muestra cómo enviar datos de control de impresora directamente a las impresoras que usan controladores de impresora basados en GDI.</span><span class="sxs-lookup"><span data-stu-id="138cc-104">The code sample later in this topic shows how to send printer control data directly to printers that use GDI-based printer drivers.</span></span>

<span data-ttu-id="138cc-105">En los pasos siguientes se describe cómo enviar datos directamente a una impresora.</span><span class="sxs-lookup"><span data-stu-id="138cc-105">The following steps describe how to send data directly to a printer.</span></span> <span data-ttu-id="138cc-106">Estos pasos también se ilustran en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="138cc-106">These steps are also illustrated in the code example that follows.</span></span>

1.  <span data-ttu-id="138cc-107">Llame a [**OpenPrinter**](openprinter.md) para obtener un identificador de la impresora.</span><span class="sxs-lookup"><span data-stu-id="138cc-107">Call [**OpenPrinter**](openprinter.md) to get a handle to the printer.</span></span>
2.  <span data-ttu-id="138cc-108">Inicialice una estructura [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) con los datos de la impresora.</span><span class="sxs-lookup"><span data-stu-id="138cc-108">Initialize a [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) structure with the printer data.</span></span>
3.  <span data-ttu-id="138cc-109">Llame a [**StartDocPrinter**](startdocprinter.md) para indicar que la aplicación va a enviar datos de documento a la impresora.</span><span class="sxs-lookup"><span data-stu-id="138cc-109">Call [**StartDocPrinter**](startdocprinter.md) to indicate that the application will be sending document data to the printer.</span></span>
4.  <span data-ttu-id="138cc-110">Llame a [**StartPagePrinter**](startpageprinter.md) para indicar que la aplicación va a enviar una nueva página a la impresora.</span><span class="sxs-lookup"><span data-stu-id="138cc-110">Call [**StartPagePrinter**](startpageprinter.md) to indicate that the application will be sending a new page to the printer.</span></span>
5.  <span data-ttu-id="138cc-111">Llame a [**WritePrinter**](writeprinter.md) para enviar los datos.</span><span class="sxs-lookup"><span data-stu-id="138cc-111">Call [**WritePrinter**](writeprinter.md) to send the data.</span></span>
6.  <span data-ttu-id="138cc-112">Llame a [**EndPagePrinter**](endpageprinter.md) para indicar que se han enviado todos los datos de la página actual.</span><span class="sxs-lookup"><span data-stu-id="138cc-112">Call [**EndPagePrinter**](endpageprinter.md) to indicate that all data for the current page has been sent.</span></span>
7.  <span data-ttu-id="138cc-113">Llame a [**EndDocPrinter**](enddocprinter.md) para indicar que se han enviado todos los datos de este documento.</span><span class="sxs-lookup"><span data-stu-id="138cc-113">Call [**EndDocPrinter**](enddocprinter.md) to indicate that all data for this document has been sent.</span></span>
8.  <span data-ttu-id="138cc-114">Llame a [**ClosePrinter**](closeprinter.md) para liberar los recursos.</span><span class="sxs-lookup"><span data-stu-id="138cc-114">Call [**ClosePrinter**](closeprinter.md) to release the resources.</span></span>

<span data-ttu-id="138cc-115">Enviar datos de control de impresora directamente a las impresoras que usan controladores de impresora basados en GDI.</span><span class="sxs-lookup"><span data-stu-id="138cc-115">Send printer control data directly to printers that use GDI-based printer drivers.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="138cc-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="138cc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="138cc-117">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="138cc-117">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="138cc-118">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="138cc-118">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="138cc-119">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="138cc-119">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="138cc-120">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="138cc-120">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="138cc-121">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="138cc-121">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="138cc-122">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="138cc-122">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="138cc-123">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="138cc-123">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 
