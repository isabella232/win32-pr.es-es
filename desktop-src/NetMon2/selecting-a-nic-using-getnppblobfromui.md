---
description: Con Monitor de red, seleccionar una NIC mediante programación es un proceso de dos pasos. En primer lugar, cree el blob de filtro mediante una llamada al método CreateBlob. A continuación, seleccione la NIC llamando al método GetNPPBlobFromUI.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Selección de una NIC mediante GetNPPBlobFromUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3bd02ef5085bba511fb0d05844840eb92d85ef83c67f244ab321570fae4ad8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128905"
---
# <a name="selecting-a-nic-using-getnppblobfromui"></a>Selección de una NIC mediante GetNPPBlobFromUI

Con Monitor de red, seleccionar una NIC mediante programación es un proceso de dos pasos. En primer lugar, cree el blob de filtro mediante una llamada [**al método CreateBlob.**](createblob.md) A continuación, seleccione la NIC mediante una llamada [**al método GetNPPBlobFromUI.**](getnppblobfromui.md)

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



 

 



