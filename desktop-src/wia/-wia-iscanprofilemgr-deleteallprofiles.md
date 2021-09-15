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
ms.openlocfilehash: f21e9f562d008846b4ecf6ad46e86c2c371eb9f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359995"
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
| Encabezado<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Esquema de perfil de examen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




