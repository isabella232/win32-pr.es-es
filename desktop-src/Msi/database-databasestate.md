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
ms.openlocfilehash: a44fcc9e082878077533edafcd44c9f5a5f26e76bddd3ddb5619fb2842ec0d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745645"
---
# <a name="databasedatabasestate-property"></a>Database.DatabaseState, propiedad

La **propiedad DatabaseState** del [**objeto Database**](database-object.md) es una propiedad de solo lectura.

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
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-00000000046<br/>                                                                                                                                                                            |



 

 




