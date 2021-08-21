---
description: La propiedad FeatureCurrentState del objeto Session es una propiedad de solo lectura que devuelve el estado instalado actual de la característica designada. Para los valores de estado, consulte la propiedad FeatureRequestState.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Propiedad Session.FeatureCurrentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3738a33d2c7a855abe6cc60139286b3e9c4d586bc6c2d9d436390fc5e52f4fd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629235"
---
# <a name="sessionfeaturecurrentstate-property"></a>Propiedad Session.FeatureCurrentState

La **propiedad FeatureCurrentState** del objeto [**Session**](session-object.md) es una propiedad de solo lectura que devuelve el estado instalado actual de la característica designada. Para los valores de estado, consulte [**la propiedad FeatureRequestState.**](session-featurerequeststate.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a>Valor de propiedad

Nombre de cadena requerido de la característica solicitada y una clave principal en la [tabla Característica](feature-table.md).

## <a name="remarks"></a>Comentarios

Si se produce un error en la propiedad , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Sesión**](session-object.md)
</dt> <dt>

[**Propiedad FeatureRequestState**](session-featurerequeststate.md)
</dt> </dl>

 

 




