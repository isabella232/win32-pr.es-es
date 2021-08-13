---
description: Elimina todos los perfiles de examen asociados al dispositivo especificado.
ms.assetid: 5abf101b-0442-47fc-8159-95db63f0af78
title: Método IScanProfileMgr::D eleteAllProfiles (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f7476f014b0dbcdb16af2a0db46c92a8c2db112528ec4bb8f2903e0c7f9c7a72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450825"
---
# <a name="iscanprofilemgrdeleteallprofiles-method"></a>IScanProfileMgr::D eleteAllProfiles (método)

Elimina todos los perfiles de examen asociados al dispositivo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteAllProfiles(
  [in] BSTR bstrDeviceID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrDeviceID* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Identificador del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




