---
description: Devuelve el GUID del perfil.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: Método IScanProfile::GetGUID (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 37d383d5975957c45b2aa5a0c90350f794e6f20deb9a7bfbe73c9f2d42b2bca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441583"
---
# <a name="iscanprofilegetguid-method"></a>IScanProfile::GetGUID (método)

Devuelve el GUID del perfil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*retVal* \[ out\]
</dt> <dd>

Tipo: **\* GUID**

Puntero al GUID del perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

El GUID de un perfil se genera automáticamente cuando se crea el perfil con [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Esquema de perfil de examen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




