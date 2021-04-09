---
description: Establece el valor de las propiedades secundarias especificadas en el <Properties> elemento de un perfil de digitalización.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'IScanProfile:: SetProperty (método) (Scanprofile. h)'
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
ms.openlocfilehash: f8f21891ae0cc5fa8e64fafd4acb9e61334a7279
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810790"
---
# <a name="iscanprofilesetproperty-method"></a>IScanProfile:: SetProperty (método)

Establece el valor de las propiedades secundarias especificadas en el `<Properties>` elemento de un perfil de digitalización.

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

*número* \[ de de\]
</dt> <dd>

Tipo: **ULong**

El número de entradas de las matrices a las que apuntan *PID* y *PVAR*.

</dd> <dt>

*PID* \[ de de\]
</dt> <dd>

Tipo: **PROPID \** _

Puntero a una matriz de números de identificación de las propiedades que se van a establecer. Cada valor de la matriz es una [constante de propiedad de WIA](-wia-wia-property-constants.md).

</dd> <dt>

_pvar * \[ en\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

Puntero a una matriz de valores que se va a asignar a las propiedades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Cada valor de la matriz al que apunta el *PID* es una de las [constantes de propiedad de WIA](-wia-wia-property-constants.md). Puede extender este sistema de identificación. Vea [definir propiedades personalizadas](-wia-defining-custom-properties.md).

Los cambios en un perfil no se guardan en el disco hasta que la aplicación llama al método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .

Si dos aplicaciones crean objetos de Perfil de análisis a partir del mismo archivo XML y cada aplicación escribe cambios en su objeto, solo los cambios realizados por la aplicación que llama a [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last se guardan en el disco.

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

**Vista**
</dt> <dt>

[Esquema de análisis de perfil](-wia-scan-profile-schema.md)
</dt> <dt>

[Constantes de propiedad de WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Definir propiedades personalizadas](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
