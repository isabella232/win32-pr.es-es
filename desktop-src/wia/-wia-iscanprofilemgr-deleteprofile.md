---
description: Elimina el perfil de examen especificado.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: Método IScanProfileMgr::D eleteProfile (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 52a4f2fc11e2a2cac1c3b3c547ee1b7a967a5441fc44cd2bb213bdbf681df8f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670258"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a>IScanProfileMgr::D eleteProfile (método)

Elimina el perfil de examen especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pScanProfile* \[ En\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\***

Puntero al perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

**IScanProfileMgr::D eleteProfile** elimina el perfil del disco y destruye el objeto de perfil en memoria.

Use el [**método IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) cuando más de un objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) pueda crear o eliminar perfiles al mismo tiempo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Esquema de perfil de examen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




