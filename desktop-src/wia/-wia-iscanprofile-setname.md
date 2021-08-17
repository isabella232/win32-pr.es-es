---
description: Establece el nombre descriptivo del perfil.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: Método IScanProfile::SetName (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 0023353f298d5b6690345d559517c3840d33da6eb836c983b85924b5c4ac4260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441486"
---
# <a name="iscanprofilesetname-method"></a>IScanProfile::SetName (método)

Establece el nombre descriptivo del perfil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrName* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Nombre descriptivo del perfil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método es necesario porque el GUID de un perfil no se puede usar para mostrar el perfil de examen a un usuario.

Un usuario puede cambiar el nombre descriptivo de un perfil con el [**método ScanProfileDialog.**](-wia-iscanprofileui-scanprofiledialog.md)

Los cambios en un perfil no se guardan en el disco hasta que la aplicación llama al [**método IScanProfile::Save.**](-wia-iscanprofile-save.md)

Si dos aplicaciones crean objetos de perfil de examen a partir del mismo archivo XML y cada aplicación escribe cambios en su objeto, solo los cambios realizados por la aplicación que llama a [**IScanProfile::Save**](-wia-iscanprofile-save.md) last se guardan en el disco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



 

 




