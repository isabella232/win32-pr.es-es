---
description: El método OpenView del objeto Database devuelve un objeto View que representa la consulta especificada por una SQL cadena.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Método Database.OpenView (Certview.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158635"
---
# <a name="databaseopenview-method"></a>Método Database.OpenView

El **método OpenView** del objeto [**Database**](database-object.md) devuelve un [**objeto View**](view-object.md) que representa la consulta especificada por una SQL cadena.

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

Se requiere SQL cadena de consulta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para obtener información sobre SQL sintaxis implementada en el instalador, vea [sintaxis SQL .](sql-syntax.md)

Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Encabezado<br/>  | <dl> <dt>Certview.h</dt> </dl>                                                                                                                                                                   |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Base de datos**](database-object.md)
</dt> <dt>

[Sintaxis de SQL](sql-syntax.md)
</dt> </dl>

 

 




