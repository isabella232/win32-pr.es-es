---
description: Elimina todos los perfiles de examen disponibles para el usuario en el sistema en el que se ejecuta la aplicación.
ms.assetid: 1a79fd0e-1309-4fc4-863f-6dfb20594d91
title: Método IScanProfileMgr::D eleteAllProfilesForUser (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfilesForUser
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 967a2ca3e2ed313c024f52cec6d8064c702c6caedc122ce7bd4409f3408ec995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209105"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a>IScanProfileMgr::D eleteAllProfilesForUser (método)

Elimina todos los perfiles de examen disponibles para el usuario en el sistema en el que se ejecuta la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Esquema de perfil de examen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




