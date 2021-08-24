---
description: Devuelve el número de elementos almacenados por este enumerador.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: Método IEnumWiaItem2::GetCount (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0a64a7c015f7c21ff19a736570aa104f0b229bc1b6561001b612045824f9a31d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882425"
---
# <a name="ienumwiaitem2getcount-method"></a>IEnumWiaItem2::GetCount (método)

Devuelve el número de elementos almacenados por este enumerador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cElt* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

Recibe un puntero a un **ULONG** que recibe el número de elementos de la enumeración .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




