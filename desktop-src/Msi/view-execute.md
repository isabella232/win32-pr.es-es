---
description: El método Execute del objeto View usa el token de signo de interrogación para representar parámetros en una instrucción SQL consulta. Para obtener más información, vea sintaxis SQL de datos. Los valores de estos parámetros se pasan como los campos correspondientes de un registro de parámetros.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exemétodo de condón
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9bfd1120382ea06f6046f4435d0143024422ff6345959099326ab4a5428d26d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804033"
---
# <a name="viewexecute-method"></a>View.Exemétodo de condón

El **método Execute** del objeto [**View**](view-object.md) usa el token de signo de interrogación para representar parámetros en una instrucción SQL consulta. Para obtener más información, [vea sintaxis SQL .](sql-syntax.md) Los valores de estos parámetros se pasan como los campos correspondientes de un registro de parámetros.

## <a name="syntax"></a>Sintaxis


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*record* 
</dt> <dd>

Objetos [**record**](record-object.md) opcionales que contienen los valores que reemplazan los tokens de parámetro (?) en la SQL consulta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Se debe llamar a este método antes de cualquier llamada al [**método Fetch.**](view-fetch.md)

Si la consulta SQL especifica valores con marcadores de parámetro (?), se debe proporcionar un registro que contenga todos los valores de reemplazo, que deben estar en el mismo orden y del mismo tipo de datos que los marcadores de parámetro. Cuando este método se usa con consultas INSERT y UPDATE, los tokens de signo de interrogación deben preceder a todos los valores sin parámetros.

Por ejemplo, estas consultas son válidas:

UPDATE {table-list} SET {column}= ? , {column}= {constant}

INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})

Sin embargo, estas consultas no son válidas:

UPDATE {table-list} SET {column}= {constant}, {column}=?

INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ? )

Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView se define como \_ 000C109C-0000-0000-C000-00000000046<br/>                                                                                                                                                                                |



 

 




