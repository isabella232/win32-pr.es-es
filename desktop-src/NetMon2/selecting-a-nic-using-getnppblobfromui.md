---
description: Con Monitor de red, seleccionar una NIC mediante programación es un proceso de dos pasos. En primer lugar, cree el blob de filtro llamando al método CreateBlob. A continuación, seleccione la NIC llamando al método GetNPPBlobFromUI.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Selección de una NIC mediante GetNPPBlobFromUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb429a87d284a5a6a03a20357728c8bbcb5acac4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074078"
---
# <a name="selecting-a-nic-using-getnppblobfromui"></a>Selección de una NIC mediante GetNPPBlobFromUI

Con Monitor de red, seleccionar una NIC mediante programación es un proceso de dos pasos. En primer lugar, cree el blob de filtro llamando al [**método CreateBlob.**](createblob.md) A continuación, seleccione la NIC llamando al [**método GetNPPBlobFromUI.**](getnppblobfromui.md)

En este ejemplo se usa un blob de filtro para seleccionar la NIC necesaria:


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



 

 



