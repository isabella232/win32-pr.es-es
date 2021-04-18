---
description: Crea un perfil de digitalización vacío y lo asocia a un escáner u otro elemento 2,0 de adquisición de imágenes de Windows (WIA).
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'IScanProfileMgr:: CreateProfile (método) (Scanprofilemgr. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497723"
---
# <a name="iscanprofilemgrcreateprofile-method"></a>IScanProfileMgr:: CreateProfile (método)

Crea un perfil de digitalización vacío y lo asocia a un escáner u otro elemento 2,0 de adquisición de imágenes de Windows (WIA).

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

*bstrDeviceID* \[ de\]
</dt> <dd>

Tipo: **BSTR**

El identificador del dispositivo o el elemento WIA 2,0.

</dd> <dt>

*bstrName* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Nombre descriptivo del nuevo perfil.

</dd> <dt>

*guidCategory* \[ de\]
</dt> <dd>

Tipo: **GUID**

El GUID de la categoría del dispositivo o el elemento WIA 2,0. Debe ser una de las constantes de \_ categoría de elemento IPA de WIA \_ \_ .

</dd> <dt>

*ppScanProfile* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Dirección de un puntero al nuevo perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

**IScanProfileMgr:: CreateProfile** asocia el dispositivo especificado con el nuevo perfil de digitalización.

**IScanProfileMgr:: CreateProfile** genera automáticamente un GUID para el nuevo perfil. Obtiene el GUID con [**GetGUID**](-wia-iscanprofile-getguid.md).

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

 

 




