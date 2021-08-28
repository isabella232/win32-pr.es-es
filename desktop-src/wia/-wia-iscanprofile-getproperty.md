---
description: Obtiene el valor de las propiedades secundarias especificadas en <Properties> elemento de un perfil de examen.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: Método IScanProfile::GetProperty (Scanprofile.h)
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
ms.openlocfilehash: ef09115c7131df21697540fa941f8bd863650bc029601088b4a0f8c80e9b1a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814085"
---
# <a name="iscanprofilegetproperty-method"></a>IScanProfile::GetProperty (método)

Obtiene el valor de las propiedades secundarias especificadas en el `<Properties>` elemento de un perfil de examen.

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

*num* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Número de entradas de las matrices a las que *apuntan pid* y *pvar.*

</dd> <dt>

*pid* \[ En\]
</dt> <dd>

Tipo: **PROPID \***

Puntero a una matriz de los números de identificación de las propiedades que se establecerán. Cada valor de la matriz es una [constante de propiedad de WIA.](-wia-wia-property-constants.md)

</dd> <dt>

*pvar* \[ out\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\***

Puntero a una matriz de valores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Devuelve S FALSE si alguno de los valores de \_ propiedad no está disponible; de lo contrario, devuelve S \_ OK o un código de error COM estándar.

## <a name="remarks"></a>Comentarios

El tipo de cada valor debe ser el mismo tipo que se estableció con la llamada a [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).

Cada valor de la matriz a la que *apunta pid* es una de las constantes de la [propiedad WIA](-wia-wia-property-constants.md). Puede ampliar este sistema de identificación. Vea [Definir propiedades personalizadas.](-wia-defining-custom-properties.md)

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

 

 
