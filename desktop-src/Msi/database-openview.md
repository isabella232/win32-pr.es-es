---
description: El método OpenView del objeto de base de datos devuelve un objeto de vista que representa la consulta especificada por una cadena SQL.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Método Database. OpenView (Certview. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653983"
---
# <a name="databaseopenview-method"></a>Database. OpenView (método)

El método **OpenView** del objeto de [**base de datos**](database-object.md) devuelve un objeto de [**vista**](view-object.md) que representa la consulta especificada por una cadena SQL.

## <a name="syntax"></a>Sintaxis


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sql* 
</dt> <dd>

Cadena de consulta SQL necesaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para obtener información sobre la sintaxis de SQL implementada en el instalador, vea [Sintaxis de SQL](sql-syntax.md).

Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Encabezado<br/>  | <dl> <dt>Certview. h</dt> </dl>                                                                                                                                                                   |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Base de datos**](database-object.md)
</dt> <dt>

[Sintaxis de SQL](sql-syntax.md)
</dt> </dl>

 

 




