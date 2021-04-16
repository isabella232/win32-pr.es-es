---
description: Obtiene el GUID de la categoría del elemento 2,0 de adquisición de imágenes de Windows (WIA) al que está asociado el perfil.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: 'IScanProfile:: GetItem (método) (Scanprofile. h)'
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
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652475"
---
# <a name="iscanprofilegetitem-method"></a>IScanProfile:: GetItem (método)

Obtiene el GUID de la categoría del elemento 2,0 de adquisición de imágenes de Windows (WIA) al que está asociado el perfil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pguidCategory* \[ enuncia\]
</dt> <dd>

Tipo: **GUID \** _

Un puntero al GUID de la categoría del elemento de WIA 2,0. Siempre es una de las constantes de \_ categoría del elemento IPA de WIA \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

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

 

 




