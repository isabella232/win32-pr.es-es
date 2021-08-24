---
description: Obtiene un valor que indica si el perfil es el perfil de examen predeterminado de un dispositivo IWiaItem2 asociado.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: Método IScanProfile::IsDefault (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 3f763286a6db8430514cd70bc05eb160935e0fdc7ae8b5c452e8c09a113c0af5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882415"
---
# <a name="iscanprofileisdefault-method"></a>IScanProfile::IsDefault (método)

Obtiene un valor que indica si el perfil es el perfil de examen predeterminado de un [**dispositivo IWiaItem2**](-wia-iwiaitem2.md) asociado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbDefault* \[ out\]
</dt> <dd>

Tipo: **BOOL \***

Puntero a un **objeto BOOL.**

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdad**


</dt> <dd>

El perfil es el valor predeterminado.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**Falso**


</dt> <dd>

El perfil no es el valor predeterminado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

*pbDefault* es **TRUE** si el perfil contiene un `<Default>` elemento . Es **FALSE si** no hay ningún elemento de este tipo. El elemento no tiene ningún valor.

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

 

 




