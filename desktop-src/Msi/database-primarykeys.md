---
description: La propiedad PrimaryKeys del objeto Database devuelve un objeto Record que contiene el nombre de tabla en el campo 0 y los nombres de columna (que comprenden las claves principales) en los campos siguientes correspondientes a sus números de columna.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Database.PrimaryKeys, propiedad
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158634"
---
# <a name="databaseprimarykeys-property"></a>Database.PrimaryKeys, propiedad

La **propiedad PrimaryKeys** del objeto [**Database**](database-object.md) devuelve un objeto [**Record**](record-object.md) que contiene el nombre de tabla en el campo 0 y los nombres de columna (que comprenden las claves principales) en los campos siguientes correspondientes a sus números de columna. El recuento de campos del registro es el recuento de columnas de clave principal.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a>Valor de propiedad

Nombre necesario de una tabla existente. Se genera un error si la tabla no existe.

## <a name="remarks"></a>Observaciones

La **propiedad PrimaryKeys** no se puede usar con la [ \_ tabla Tables ni](-tables-table.md) con la tabla [ \_ Columns](-columns-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




