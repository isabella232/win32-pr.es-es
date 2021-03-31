---
description: Quita una lista especificada de propiedades secundarias en el <Properties> elemento de un perfil de digitalización.
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'IScanProfile:: RemoveProperty (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154872"
---
# <a name="iscanprofileremoveproperty-method"></a>IScanProfile:: RemoveProperty (método)

Quita una lista especificada de propiedades secundarias en el `<Properties>` elemento de un perfil de digitalización.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*número* \[ de de\]
</dt> <dd>

Tipo: **ULong**

Número de entradas de la matriz a la que señala el *PID* .

</dd> <dt>

*PID* \[ de de\]
</dt> <dd>

Tipo: **PROPID \** _

Puntero a una matriz de números de identificación de las propiedades que se van a eliminar. Cada una de ellas es una [constante de propiedad de WIA](-wia-wia-property-constants.md).

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

 

 




