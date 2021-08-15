---
description: Obtiene todos los iDs de propiedad disponibles en un perfil.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: Método IScanProfile::GetAllPropIDs (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 7fd54e3e1cd45c3631df9b069ddf3c2e897037efb2870d00946f0a002e12f145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965784"
---
# <a name="iscanprofilegetallpropids-method"></a>IScanProfile::GetAllPropIDs (método)

Obtiene todos los iDs de propiedad disponibles en un perfil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*num* \[ in, out\]
</dt> <dd>

Tipo: **ULONG \***

Número de identificaciónes de propiedad solicitadas o devueltas.

</dd> <dt>

*ppid* \[ out\]
</dt> <dd>

Tipo: **PROPID \***

Puntero a una matriz de los ID de propiedad.

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

 

 




