---
description: Guarda los cambios en un perfil en el disco.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: Método IScanProfile::Save (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 7cf4201a0d149c7b529e595d7f2c2ea92a6010f6cffd3e6c5c74fb3cdc040651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450925"
---
# <a name="iscanprofilesave-method"></a>IScanProfile::Save (método)

Guarda los cambios en un perfil en el disco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Un perfil de examen guardado es un archivo XML almacenado en %USERPROFILE% \\ Application Data Microsoft Document Center \\ \\ \\ UserScanProfiles.

Si más de un proceso escribe en el objeto [**IScanProfile,**](-wia-iscanprofile.md) el que llama a **IScanProfile::Save** last es el único proceso cuyos cambios se guardan.

El **método IScanProfile::Save** valida el perfil antes de guardarlo. El perfil siempre se considera válido a menos que la categoría del elemento de adquisición de imágenes de Windows (WIA) 2.0 asociado al perfil sea WIA CATEGORY FLATBED o \_ \_ WIA \_ CATEGORY \_ FEEDER. Si la categoría es WIA CATEGORY FLATBED o \_ \_ WIA \_ CATEGORY FEEDER, las siguientes propiedades deben ser válidas para el elemento, si las propiedades están contenidas \_ en el perfil:

WIA \_ IPS \_ BRIGHTNESS

CONTRASTE \_ DE IPS DE WIA \_

TIPO DE \_ DATOS IPA DE WIA \_

WIA \_ IPS \_ XRES

FORMATO \_ IPA DE WIA \_

Además, si la categoría es WIA CATEGORY FEEDER, la propiedad WIA IPS PAGE SIZE debe ser válida, si está \_ \_ presente en el \_ \_ \_ perfil. Para obtener más información sobre estas propiedades, vea [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).

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

 

 




