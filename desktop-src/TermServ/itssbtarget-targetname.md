---
title: Propiedad TargetName de ITsSbTarget
description: Especifica o recupera el nombre del destino.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Propiedad TargetName Servicios de Escritorio remoto
- Propiedad TargetName Servicios de Escritorio remoto, interfaz ITsSbTarget
- Servicios de Escritorio remoto de la interfaz ITsSbTarget, propiedad TargetName
- Propiedad TargetName Servicios de Escritorio remoto, interfaz ITsSbTargetEx
- Servicios de Escritorio remoto de la interfaz ITsSbTargetEx, propiedad TargetName
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dce949abee4ca00184a2b784ab154dbd75b9de6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076927"
---
# <a name="itssbtargettargetname-property"></a>ITsSbTarget:: TargetName (propiedad)

Especifica o recupera el nombre del destino.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Variable **BSTR** que especifica el nombre de destino.

## <a name="remarks"></a>Observaciones

Esta propiedad era de solo lectura antes de Windows Server 2012.

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

 

 





