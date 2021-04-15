---
description: Con Monitor de red, la selección de una NIC mediante programación es un proceso de dos pasos. En primer lugar, cree el BLOB de filtro llamando al método CreateBlob. A continuación, seleccione la NIC llamando al método GetNPPBlobFromUI.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Selección de una NIC mediante GetNPPBlobFromUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb429a87d284a5a6a03a20357728c8bbcb5acac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677423"
---
# <a name="selecting-a-nic-using-getnppblobfromui"></a><span data-ttu-id="36c68-105">Selección de una NIC mediante GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="36c68-105">Selecting a NIC Using GetNPPBlobFromUI</span></span>

<span data-ttu-id="36c68-106">Con Monitor de red, la selección de una NIC mediante programación es un proceso de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="36c68-106">With Network Monitor, selecting a NIC programmatically is a two-step process.</span></span> <span data-ttu-id="36c68-107">En primer lugar, cree el BLOB de filtro llamando al método [**CreateBlob**](createblob.md) .</span><span class="sxs-lookup"><span data-stu-id="36c68-107">First, create the filter BLOB by calling the [**CreateBlob**](createblob.md) method.</span></span> <span data-ttu-id="36c68-108">A continuación, seleccione la NIC llamando al método [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="36c68-108">Then, select the NIC by calling the [**GetNPPBlobFromUI**](getnppblobfromui.md) method.</span></span>

<span data-ttu-id="36c68-109">En este ejemplo, se usa un BLOB de filtro para seleccionar la NIC necesaria:</span><span class="sxs-lookup"><span data-stu-id="36c68-109">In this example a filter BLOB is used to select the required NIC:</span></span>


```C++
DWORD rc;

// Call CreateBlob to create a filter blob.
///////////////////////////////////////////
HBLOB hFilterBlob;
rc = CreateBlob(&hFilterBlob);
if (FAILED (rc));
{
  // Failed creating filter BLOB. Add appropriate error handling.
}


// Call GetNPPBlobFromUI to retrieve the NPP Blob.
//////////////////////////////////////////////////
rc = GetNPPBlobFromUI(hwnd,
                      hFilterBlob,
                      &hBlob);
if (FAILED (rc));
{
  // Failed retrieving NPP BLOB. Add appropriate error handling.
}
```



 

 



