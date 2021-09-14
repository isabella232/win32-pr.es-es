---
description: La propiedad DatabaseState del objeto Database es una propiedad de solo lectura.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Database.DatabaseState, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12a667bf145ea00f7a881c8219987f21c99af4ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158650"
---
# <a name="databasedatabasestate-property"></a>Database.DatabaseState, propiedad

La **propiedad DatabaseState** del objeto [**Database**](database-object.md) es una propiedad de solo lectura.

Esta propiedad devuelve el estado de persistencia de la base de datos como uno de los parámetros siguientes.



| Estado de la base de datos        | Value | Descripción                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| msiDatabaseStateRead  | 0     | La base de datos se abre como de solo lectura. No se permiten cambios en los datos persistentes y no se guardan los datos temporales. |
| msiDatabaseStateWrite | 1     | La base de datos está totalmente operativa para lectura y escritura.                                                          |



 

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




