---
description: La propiedad FeatureCost del objeto Session devuelve la cantidad total de espacio en disco (en unidades de 512 bytes) que requiere la característica especificada y sus características primarias (hasta la raíz de la tabla Feature).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Session.FeatureCost, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 617d1695b8b472952f22737ba3f677d9320f9b4214afc3dea5a9cc5010e2b1a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629295"
---
# <a name="sessionfeaturecost-property"></a>Session.FeatureCost, propiedad

La **propiedad FeatureCost** del objeto [**Session**](session-object.md) devuelve la cantidad total de espacio en disco (en unidades de 512 bytes) que requiere la característica especificada y sus características primarias (hasta la raíz de la tabla Feature). Para cada característica, el costo total se suma a los costos de disco atribuidos a cada componente vinculado a la característica.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Si se produce un error en la propiedad , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




