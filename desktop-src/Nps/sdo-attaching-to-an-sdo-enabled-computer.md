---
title: Asociar a un equipo SDO-Enabled
description: Asociar a un equipo SDO-Enabled
ms.assetid: 434e2e0c-075e-48a9-9617-bbe75716380d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d8c5609691f1d51598701953c795225c08e4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420789"
---
# <a name="attaching-to-an-sdo-enabled-computer"></a><span data-ttu-id="46906-103">Asociar a un equipo SDO-Enabled</span><span class="sxs-lookup"><span data-stu-id="46906-103">Attaching to an SDO-Enabled Computer</span></span>

<span data-ttu-id="46906-104">El código siguiente se adjunta al equipo local como un equipo SDO.</span><span class="sxs-lookup"><span data-stu-id="46906-104">The following code attaches to the local computer as an SDO computer.</span></span>


```C++
   HRESULT  hr;
   CComPtr<ISdoMachine> pSdoMachine;
   CLSID    clsid;

   hr = CLSIDFromProgID(TEXT("IAS.SdoMachine"), &clsid);
   if (FAILED(hr))
   {
      return hr;
   }

   hr = CoCreateInstance(
      clsid,
      NULL,
      CLSCTX_INPROC_SERVER,
      __uuidof(ISdoMachine),
      (void**)&pSdoMachine
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Pass NULL to specify local computer.
   //
   hr = pSdoMachine->Attach(NULL); 
   if (FAILED(hr))
   {
      return hr;
   }

```



<span data-ttu-id="46906-105">La conexión a un equipo como un equipo SDO es el primer paso para administrar el equipo a través de SDO.</span><span class="sxs-lookup"><span data-stu-id="46906-105">Attaching to a computer as an SDO computer is the first step in administering the computer through SDO.</span></span>

<span data-ttu-id="46906-106">Para obtener más información, vea [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine), [**ISdoMachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach).</span><span class="sxs-lookup"><span data-stu-id="46906-106">For more information, see [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine), [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach).</span></span>

 

 