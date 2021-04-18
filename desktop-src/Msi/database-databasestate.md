---
description: La propiedad DatabaseState del objeto de base de datos es una propiedad de solo lectura.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Propiedad Database. DatabaseState
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653489"
---
# <a name="databasedatabasestate-property"></a>Propiedad Database. DatabaseState

La propiedad **DatabaseState** del objeto de [**base de datos**](database-object.md) es una propiedad de solo lectura.

Esta propiedad devuelve el estado de persistencia de la base de datos como uno de los parámetros siguientes.



| Estado de base de datos        | Value | Descripción                                                                                                |
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
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




