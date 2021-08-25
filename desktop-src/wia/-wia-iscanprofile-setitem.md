---
description: Establece el GUID de la categoría de Windows adquisición de imágenes (WIA) 2.0 al que está asociado el perfil.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: Método IScanProfile::SetItem (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: fc4f79c44ff84bef1efbda4b09beee6b7dcf83f04023a5e2211e9f808b18446a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814075"
---
# <a name="iscanprofilesetitem-method"></a>IScanProfile::SetItem (método)

Establece el GUID de la categoría de Windows adquisición de imágenes (WIA) 2.0 al que está asociado el perfil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*guidCategory* \[ En\]
</dt> <dd>

Tipo: **GUID**

GUID de la categoría del elemento WIA 2.0. Debe ser una de las constantes \_ IPA ITEM CATEGORY de \_ WIA. \_

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Los usuarios pueden cambiar la categoría con [**el método ScanProfileDialog.**](-wia-iscanprofileui-scanprofiledialog.md)

Los cambios en un perfil no se guardan en el disco hasta que la aplicación llama al [**método IScanProfile::Save.**](-wia-iscanprofile-save.md)

Si dos aplicaciones crean objetos de perfil de examen a partir del mismo archivo XML y cada aplicación escribe cambios en su objeto, solo los cambios realizados por la aplicación que llama a [**IScanProfile::Save**](-wia-iscanprofile-save.md) last se guardan en el disco.

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

 

 




