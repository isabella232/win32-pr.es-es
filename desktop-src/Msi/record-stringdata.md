---
description: La propiedad StringData del objeto Record es una propiedad de lectura y escritura que transfiere los datos de cadena dentro o fuera de un campo especificado dentro del registro. Si se ha almacenado un entero o un objeto, se devuelve su valor de cadena.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Propiedad record. StringData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670965"
---
# <a name="recordstringdata-property"></a>Propiedad record. StringData

La propiedad **StringData** del objeto [**Record**](record-object.md) es una propiedad de lectura y escritura que transfiere los datos de cadena dentro o fuera de un campo especificado dentro del registro. Si se ha almacenado un entero o un objeto, se devuelve su valor de cadena.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Número de campo obligatorio del valor dentro del registro, basado en 1.

## <a name="remarks"></a>Observaciones

El valor devuelto de un campo inexistente es una cadena vacía. Para establecer un campo de cadena de registro en null, use una variante vacía o una cadena vacía. Si se intenta almacenar un valor en un campo que no existe, se producirá un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




