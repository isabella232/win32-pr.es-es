---
description: Esta es la propiedad IntegerData del objeto de registro. Esta propiedad de lectura y escritura transfiere datos enteros de 32 bits dentro o fuera de un campo especificado en el registro. Si un valor de campo no se puede convertir en un entero, se devuelve msiDatabaseNullInteger.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Propiedad record. IntegerData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653675"
---
# <a name="recordintegerdata-property"></a>Propiedad record. IntegerData

Esta es la propiedad **IntegerData** del objeto de [**registro**](record-object.md) . Esta propiedad de lectura y escritura transfiere datos enteros de 32 bits dentro o fuera de un campo especificado en el registro. Si un valor de campo no se puede convertir en un entero, se devuelve msiDatabaseNullInteger.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Número de campo obligatorio del valor dentro del registro, basado en 1.

## <a name="remarks"></a>Observaciones

Para establecer un campo de entero de registro en null, use msiDatabaseNullInteger. El valor devuelto de un campo inexistente es msiDatabaseNullInteger. Si se intenta almacenar un valor en un campo que no existe, se producirá un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




