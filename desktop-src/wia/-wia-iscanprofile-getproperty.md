---
description: Obtiene el valor de las propiedades secundarias especificadas en el <Properties> elemento de un perfil de digitalización.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: 'IScanProfile:: GetProperty (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 48137e61d88d580ac556220b4e47b949d9e2c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720402"
---
# <a name="iscanprofilegetproperty-method"></a>IScanProfile:: GetProperty (método)

Obtiene el valor de las propiedades secundarias especificadas en el `<Properties>` elemento de un perfil de digitalización.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
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

Puntero a una matriz de los números de identificación de las propiedades que se van a establecer. Cada valor de la matriz es una [constante de propiedad de WIA](-wia-wia-property-constants.md).

</dd> <dt>

_pvar * \[ out\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

Puntero a una matriz de valores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Devuelve S \_ false si alguno de los valores de propiedad no está disponible; de lo contrario, devuelve s \_ OK o un código de error com estándar.

## <a name="remarks"></a>Observaciones

El tipo de cada valor debe ser del mismo tipo que se estableció con la llamada a [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).

Cada valor de la matriz al que apunta el *PID* es una de las [constantes de propiedad de WIA](-wia-wia-property-constants.md). Puede extender este sistema de identificación. Vea [definir propiedades personalizadas](-wia-defining-custom-properties.md).

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

 

 
