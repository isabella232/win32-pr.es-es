---
description: Obtiene el GUID de la categoría del elemento Windows Image Acquisition (WIA) 2.0 al que está asociado el perfil.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: Método IScanProfile::GetItem (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 5a7f52a2d89bbd35b59febb25528fe493c4b5646afc70251fc19978d6d6265db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451045"
---
# <a name="iscanprofilegetitem-method"></a>IScanProfile::GetItem (método)

Obtiene el GUID de la categoría del elemento Windows Image Acquisition (WIA) 2.0 al que está asociado el perfil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pguidCategory* \[ out\]
</dt> <dd>

Tipo: **\* GUID**

Puntero al GUID de la categoría del elemento WIA 2.0. Esta es siempre una de las constantes ITEM CATEGORY de WIA \_ \_ \_ IPA.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

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

 

 




