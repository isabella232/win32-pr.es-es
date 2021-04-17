---
description: La propiedad FeatureCost del objeto de sesión devuelve la cantidad total de espacio en disco (en unidades de 512 bytes) que requiere la característica especificada y sus características principales (hasta la raíz de la tabla de características).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Propiedad Session. FeatureCost
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
ms.openlocfilehash: 25c93ce0b3b4efa91a827217d221546e8bab5744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653703"
---
# <a name="sessionfeaturecost-property"></a>Propiedad Session. FeatureCost

La propiedad **FeatureCost** del objeto de [**sesión**](session-object.md) devuelve la cantidad total de espacio en disco (en unidades de 512 bytes) que requiere la característica especificada y sus características principales (hasta la raíz de la tabla de características). Para cada característica, el costo total se compone de los costos de disco atribuidos a cada componente vinculado a la característica.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




