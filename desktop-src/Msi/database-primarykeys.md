---
description: La propiedad PrimaryKeys del objeto de base de datos devuelve un objeto de registro que contiene el nombre de tabla en el campo 0 y los nombres de columna (que comprenden las claves principales) en los campos que corresponden a sus números de columna.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Propiedad Database. PrimaryKeys
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671680"
---
# <a name="databaseprimarykeys-property"></a>Propiedad Database. PrimaryKeys

La propiedad **PrimaryKeys** del objeto de [**base de datos**](database-object.md) devuelve un objeto de [**registro**](record-object.md) que contiene el nombre de tabla en el campo 0 y los nombres de columna (que comprenden las claves principales) en los campos que corresponden a sus números de columna. El recuento de campos del registro es el recuento de las columnas de clave principal.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a>Valor de propiedad

Nombre necesario de una tabla existente. Si la tabla no existe, se genera un error.

## <a name="remarks"></a>Observaciones

La propiedad **PrimaryKeys** no se puede usar con [ \_ la tabla TABLES o la](-tables-table.md) [ \_ tabla Columns](-columns-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




