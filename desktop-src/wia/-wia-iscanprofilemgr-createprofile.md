---
description: Crea un perfil de examen vacío y lo asocia a un analizador u otro Windows adquisición de imágenes (WIA) 2.0.
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: Método IScanProfileMgr::CreateProfile (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359996"
---
# <a name="iscanprofilemgrcreateprofile-method"></a>IScanProfileMgr::CreateProfile (método)

Crea un perfil de examen vacío y lo asocia a un analizador u otro Windows adquisición de imágenes (WIA) 2.0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrDeviceID* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Identificador del dispositivo o del elemento de WIA 2.0.

</dd> <dt>

*bstrName* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Nombre descriptivo del nuevo perfil.

</dd> <dt>

*guidCategory* \[ En\]
</dt> <dd>

Tipo: **GUID**

GUID de la categoría del dispositivo o del elemento de WIA 2.0. Debe ser una de las constantes \_ IPA ITEM CATEGORY de \_ WIA. \_

</dd> <dt>

*ppScanProfile* \[ out\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Dirección de un puntero al nuevo perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

**IScanProfileMgr::CreateProfile** asocia el dispositivo especificado con el nuevo perfil de examen.

**IScanProfileMgr::CreateProfile** genera automáticamente un GUID para el nuevo perfil. Obtenga el GUID con [**GetGUID.**](-wia-iscanprofile-getguid.md)

Use el [**método IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) cuando más de un objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) pueda crear o eliminar perfiles al mismo tiempo.

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

 

 




