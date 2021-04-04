---
description: Obtiene todos los perfiles de digitalización disponibles para el usuario en el sistema en el que se ejecuta la aplicación.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'IScanProfileMgr:: GetProfiles (método) (Scanprofilemgr. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813883"
---
# <a name="iscanprofilemgrgetprofiles-method"></a>IScanProfileMgr:: GetProfiles (método)

Obtiene todos los perfiles de digitalización disponibles para el usuario en el sistema en el que se ejecuta la aplicación.

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

Tipo: **ULong \** _

Cuando se pasa, puntero al número máximo de perfiles que se van a devolver. Cuando se devuelve, un puntero al número de perfiles devueltos.

</dd> <dt>

_ppScanProfile * \[ out\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Dirección de una matriz de punteros a perfiles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Si el número total de perfiles disponibles para el usuario es menor que el valor pasado a *pulNumProfiles*, *pulNumProfiles* devuelve ese total. De lo contrario, devuelve el mismo valor que se le ha pasado.

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

 

 




