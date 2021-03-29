---
title: Propiedad FarmName de ITsSbTarget
description: Recupera o especifica el nombre de la granja a la que está unida este destino.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad FarmName
- Propiedad FarmName Servicios de Escritorio remoto, interfaz ITsSbTarget
- Servicios de Escritorio remoto de la interfaz ITsSbTarget, propiedad FarmName
- Propiedad FarmName Servicios de Escritorio remoto, interfaz ITsSbTargetEx
- Servicios de Escritorio remoto de la interfaz ITsSbTargetEx, propiedad FarmName
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94f86b2cf0ec257be9fe9b801e6fceae364a46e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783856"
---
# <a name="itssbtargetfarmname-property"></a>ITsSbTarget:: FarmName (propiedad)

Recupera o especifica el nombre de la granja a la que está unida este destino.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Una variable **BSTR** que contiene el nombre de la granja.

## <a name="requirements"></a>Requisitos



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Cliente mínimo compatible<br/></td>
<td>No se admite ninguno<br/></td>
</tr>
<tr class="even">
<td>Servidor mínimo compatible<br/></td>
<td>Windows Server 2012<br/></td>
</tr>
<tr class="odd">
<td>IDL<br/></td>
<td><dl> <dt>Sbtsv. idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget se define como:
<ul>
<li>16616ECC-272D-411D-B324-126893033856</li>
<li>e85e10ea-db0b-4752-B456-5fd5840901c0 en Windows Server 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





