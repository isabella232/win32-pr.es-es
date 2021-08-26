---
description: Esta es la propiedad IntegerData del objeto Record. Esta propiedad de lectura y escritura transfiere datos enteros de 32 bits dentro o fuera de un campo especificado dentro del registro. Si un valor de campo no se puede convertir en un entero, se devuelve msiDatabaseNullInteger.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Propiedad Record.IntegerData
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
ms.openlocfilehash: b3593f31d8f8cea6278346e8c99bb9c9b880aed273ae7ab70614ade112cd8c8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912925"
---
# <a name="recordintegerdata-property"></a>Propiedad Record.IntegerData

Esta es la **propiedad IntegerData** del [**objeto Record.**](record-object.md) Esta propiedad de lectura y escritura transfiere datos enteros de 32 bits dentro o fuera de un campo especificado dentro del registro. Si un valor de campo no se puede convertir en un entero, se devuelve msiDatabaseNullInteger.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Número de campo requerido del valor dentro del registro, basado en 1.

## <a name="remarks"></a>Comentarios

Para establecer un campo entero de registro en null, use msiDatabaseNullInteger. El valor devuelto de un campo inexistente es msiDatabaseNullInteger. Si se intenta almacenar un valor en un campo inexistente, se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IRecord se define como \_ 000C1093-0000-0000-C000-00000000046<br/>                                                                                                                                                                              |



 

 




