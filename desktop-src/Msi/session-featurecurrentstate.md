---
description: La propiedad FeatureCurrentState del objeto de sesión es una propiedad de solo lectura que devuelve el estado instalado actual de la característica designada. Para los valores de estado, consulte la propiedad FeatureRequestState.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Propiedad Session. FeatureCurrentState
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
ms.openlocfilehash: 47c834571dd211dd085ed94e9d8c1ff9d5516c9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680408"
---
# <a name="sessionfeaturecurrentstate-property"></a>Propiedad Session. FeatureCurrentState

La propiedad **FeatureCurrentState** del objeto de [**sesión**](session-object.md) es una propiedad de solo lectura que devuelve el estado instalado actual de la característica designada. Para los valores de estado, consulte la propiedad [**FeatureRequestState**](session-featurerequeststate.md) .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a>Valor de propiedad

Nombre de cadena requerido de la característica solicitada y una clave principal en la [tabla de características](feature-table.md).

## <a name="remarks"></a>Observaciones

Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**De sesión**](session-object.md)
</dt> <dt>

[**Propiedad FeatureRequestState**](session-featurerequeststate.md)
</dt> </dl>

 

 




