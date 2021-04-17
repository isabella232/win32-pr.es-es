---
description: Devuelve el GUID del perfil.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: 'IScanProfile:: GetGUID (método) (Scanprofile. h)'
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
ms.openlocfilehash: e3c39815e1bc88830f64f632689028c4c527a710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360401"
---
# <a name="iscanprofilegetguid-method"></a>IScanProfile:: GetGUID (método)

Devuelve el GUID del perfil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*retval* \[ enuncia\]
</dt> <dd>

Tipo: **GUID \** _

Puntero al GUID del perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El GUID de un perfil se genera automáticamente cuando se crea el perfil con [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Esquema de análisis de perfil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




