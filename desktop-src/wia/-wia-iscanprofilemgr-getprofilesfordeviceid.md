---
description: Obtiene todos los perfiles de examen asociados a un dispositivo.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: Método IScanProfileMgr::GetProfilesforDeviceID (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 10a7d891a114fc36de3f91341febf1616a06ed22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466537"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a>IScanProfileMgr::GetProfilesforDeviceID (método)

Obtiene todos los perfiles de examen asociados a un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrDeviceID* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Identificador del dispositivo.

</dd> <dt>

*pulNumProfiles* \[ in, out\]
</dt> <dd>

Tipo: **ULONG \***

Cuando se pasa, un puntero al número máximo de perfiles que se devolverán. Cuando se devuelve, puntero al número de perfiles devueltos.

</dd> <dt>

*ppScanProfile* \[ out\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Dirección de un puntero a una matriz de perfiles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Si el número total de perfiles asociados al dispositivo es menor que el valor pasado a *pulNumProfiles,* *pulNumProfiles* devuelve ese total. De lo contrario, devuelve el mismo valor que se le pasó.

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

 

 




