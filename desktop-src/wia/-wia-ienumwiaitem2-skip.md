---
description: Omite el número especificado de elementos durante una enumeración de objetos IWiaItem2 disponibles.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: Método IEnumWiaItem2::Skip (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e8676f997ea509bc6a6632a38230b16cf5477ef807f0de25d1505afd462fe834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814255"
---
# <a name="ienumwiaitem2skip-method"></a>IEnumWiaItem2::Skip (método)

Omite el número especificado de elementos durante una enumeración de objetos [**IWiaItem2**](-wia-iwiaitem2.md) disponibles.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cElt* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Especifica el número de elementos que se omitirán.

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



 

 




