---
description: Establece el valor de las propiedades secundarias especificadas en <Properties> elemento de un perfil de examen.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: Método IScanProfile::SetProperty (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: ba4c7aff5139f1230179299d80065f1b933a6cf2d01d4ca03c045ccbe142c3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441431"
---
# <a name="iscanprofilesetproperty-method"></a>IScanProfile::SetProperty (método)

Establece el valor de las propiedades secundarias especificadas en el `<Properties>` elemento de un perfil de examen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*num* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Número de entradas de las matrices a las que *apuntan pid* y *pvar.*

</dd> <dt>

*pid* \[ En\]
</dt> <dd>

Tipo: **PROPID \***

Puntero a una matriz de números de identificación de las propiedades que se establecerán. Cada valor de la matriz es una [constante de propiedad de WIA.](-wia-wia-property-constants.md)

</dd> <dt>

*pvar* \[ En\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\***

Puntero a una matriz de valores que se asignarán a las propiedades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Cada valor de la matriz a la que *apunta pid* es una de las constantes de la [propiedad WIA](-wia-wia-property-constants.md). Puede ampliar este sistema de identificación. Vea [Definir propiedades personalizadas.](-wia-defining-custom-properties.md)

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

**Conceptual**
</dt> <dt>

[Esquema de perfil de examen](-wia-scan-profile-schema.md)
</dt> <dt>

[Constantes de propiedad WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Definir propiedades personalizadas](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
