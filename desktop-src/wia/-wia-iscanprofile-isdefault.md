---
description: Obtiene un valor que indica si el perfil es el perfil de detección predeterminado de un dispositivo IWiaItem2 asociado.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'IScanProfile:: IsDefault (método) (Scanprofile. h)'
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
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001303"
---
# <a name="iscanprofileisdefault-method"></a>IScanProfile:: IsDefault (método)

Obtiene un valor que indica si el perfil es el perfil de detección predeterminado de un dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) asociado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbDefault* \[ enuncia\]
</dt> <dd>

Tipo: **bool \** _

Un puntero a un _ * BOOL * *.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**REALES**


</dt> <dd>

El perfil es el predeterminado.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**ES**


</dt> <dd>

El perfil no es el valor predeterminado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

*pbDefault* es **true** si el perfil contiene un `<Default>` elemento. Es **false** si no existe ningún elemento de este tipo. El elemento no tiene ningún valor.

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

 

 




