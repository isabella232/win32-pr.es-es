---
description: Obtiene el número de identificaciónes de propiedad de un perfil.
ms.assetid: fa587c8a-8d09-4dfc-938a-5ec8cc9265f5
title: Método IScanProfile::GetNumPropIDS (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetNumPropIDS
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: b8193259844732b708e56ba5fb191bd9ed7f9bf8fac27609c256b4df9cc7ccb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441485"
---
# <a name="iscanprofilegetnumpropids-method"></a>IScanProfile::GetNumPropIDS (método)

Obtiene el número de identificaciónes de propiedad de un perfil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNumPropIDS(
  [out] ULONG *num
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*num* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

Número de identificaciónes de propiedad en el perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Esquema de perfil de examen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




