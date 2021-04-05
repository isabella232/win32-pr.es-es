---
description: En el siguiente código de ejemplo, el monitor establece un filtro de captura que especifica solo IP y los datos de protocolo solicitados.
ms.assetid: 0945bceb-b5fe-4f07-866b-4e0468227610
title: Procesar datos de fotogramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41c49de62d630033aa7d3ed3e8e115fd1a02f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001703"
---
# <a name="processing-frame-data"></a><span data-ttu-id="73a87-103">Procesar datos de fotogramas</span><span class="sxs-lookup"><span data-stu-id="73a87-103">Processing Frame Data</span></span>

<span data-ttu-id="73a87-104">En el siguiente código de ejemplo, el monitor establece un filtro de captura que especifica **solo IP** y los datos de protocolo solicitados.</span><span class="sxs-lookup"><span data-stu-id="73a87-104">In the following example code, the monitor sets a capture filter that specifies **IP only** and requested protocol data.</span></span>


```C++
STDMETHODIMP CTestMon::OnFrames(UPDATE_EVENT Event)
{
    DWORD i;
    LPFRAMETABLE lpFrameTable = Event.lpFrameTable;

    // The frame table can wrap the indexes.
    for (
      i = lpFrameTable->StartIndex; 
      i != lpFrameTable->EndIndex; 
     (i == lpFrameTable->FrameTableLength ) ? i=0: i ++ )
    {
        LPFRAME_DESCRIPTOR lpFrameDesc = &lpFrameTable->Frames[i];
        
        // Cast the frame data to an unaligned pointer to an IP  
        // structure. A try/catch block could be a workaround, but
        // if the capture filter is set correctly, this is the
        // verifiable IP.
        ULPIP ulpIP = (ULPIP)(&lpFrameDesc->FramePointer[lpFrameDesc->LowProtocolOffset]);
        // Now examine the IP frame.
    }
    return NOERROR;
}
```



 

 



