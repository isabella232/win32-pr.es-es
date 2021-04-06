---
description: Elimina el perfil de digitalización especificado.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: IScanProfileMgr::D método eleteProfile (Scanprofilemgr. h)
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
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002036"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a>IScanProfileMgr::D método eleteProfile

Elimina el perfil de digitalización especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pScanProfile* \[ de\]
</dt> <dd>

Tipo: **[**IScanProfile**](-wia-iscanprofile.md) \** _

Puntero al perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

**IScanProfileMgr::D eleteprofile** elimina el perfil del disco y destruye el objeto de perfil en la memoria.

Use el método [**IScanProfileMgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) cuando más de un objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) pueda estar creando o eliminando perfiles al mismo tiempo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Esquema de análisis de perfil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




