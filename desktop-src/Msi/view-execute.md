---
description: El método Execute del objeto View utiliza el token de signo de interrogación para representar los parámetros en una instrucción SQL. Para obtener más información, vea sintaxis de SQL. Los valores de estos parámetros se pasan como los campos correspondientes de un registro de parámetros.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exe(método)
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
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653363"
---
# <a name="viewexecute-method"></a>View.Exe(método)

El método **Execute** del objeto [**View**](view-object.md) utiliza el token de signo de interrogación para representar los parámetros en una instrucción SQL. Para obtener más información, vea [Sintaxis de SQL](sql-syntax.md). Los valores de estos parámetros se pasan como los campos correspondientes de un registro de parámetros.

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

Objetos de [**registro**](record-object.md) opcionales que contienen los valores que reemplazan los tokens de parámetro (?) en la consulta SQL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se debe llamar a este método antes de cualquier llamada al método [**Fetch**](view-fetch.md) .

Si la consulta SQL especifica valores con marcadores de parámetros (?), se debe proporcionar un registro que contenga todos los valores de reemplazo, que deben estar en el mismo orden y del mismo tipo de datos que los marcadores de parámetros. Cuando este método se usa con consultas INSERT y UPDATE, los tokens de signo de interrogación deben preceder a todos los valores sin parámetros.

Por ejemplo, estas consultas son válidas:

Actualice {Table-List} SET {Column} =? , {Column} = {Constant}

Inserte INTO {Table} ({Column-List}) VALUEs (?, {Constant-List})

Sin embargo, estas consultas no son válidas:

Actualice {Table-List} SET {Column} = {Constant}, {Column} =?

Inserte INTO {Table} ({Column-List}) VALUEs ({Constant-List},? )

Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView se define como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




