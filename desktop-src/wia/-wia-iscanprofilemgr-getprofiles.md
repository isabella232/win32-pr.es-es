---
description: Obtiene todos los perfiles de examen disponibles para el usuario en el sistema en el que se ejecuta la aplicación.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: Método IScanProfileMgr::GetProfiles (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466538"
---
# <a name="iscanprofilemgrgetprofiles-method"></a>IScanProfileMgr::GetProfiles (método)

Obtiene todos los perfiles de examen disponibles para el usuario en el sistema en el que se ejecuta la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulNumProfiles* \[ in, out\]
</dt> <dd>

Tipo: **ULONG \***

Cuando se pasa, un puntero al número máximo de perfiles que se devolverán. Cuando se devuelve, un puntero al número de perfiles devueltos.

</dd> <dt>

*ppScanProfile* \[ out\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Dirección de una matriz de punteros a perfiles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Si el número total de perfiles disponibles para el usuario es menor que el valor pasado a *pulNumProfiles,* *pulNumProfiles* devuelve ese total. De lo contrario, devuelve el mismo valor que se le pasó.

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

 

 




