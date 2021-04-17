---
description: La \_ tabla de columnas es una tabla del sistema de solo lectura que contiene el catálogo de columnas. Muestra las columnas de todas las tablas. Puede consultar esta tabla para averiguar si existe una columna determinada.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: _Columns tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667084"
---
# <a name="_columns-table"></a>\_Tabla de columnas

La \_ tabla de columnas es una tabla del sistema de solo lectura que contiene el catálogo de columnas. Muestra las columnas de todas las tablas. Puede consultar esta tabla para averiguar si existe una columna determinada.

La \_ tabla de columnas tiene las columnas siguientes.



| Columna | Tipo                   | Clave | Nullable |
|--------|------------------------|-----|----------|
| Tabla  | [Texto](text.md)       | Y   | N        |
| Number | [Entero](integer.md) | Y   | N        |
| Nombre   | [Texto](text.md)       | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro
</dt> <dd>

El nombre de la tabla que contiene la columna.

</dd> <dt>

<span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Números
</dt> <dd>

El orden de la columna dentro de la tabla.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

El nombre de la columna.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Dado \_ que la tabla de columnas es una tabla del sistema que no se puede modificar mediante consultas SQL, no puede obtener las claves principales con la función [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) o la [**propiedad PrimaryKeys**](database-primarykeys.md).

Solo las columnas persistentes se almacenan en la \_ tabla de columnas. Para determinar si existe una columna temporal, es necesario crear una vista mediante una instrucción SELECT \* en la tabla y, a continuación, recorrer todos los campos de un registro devueltos por la función [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) con la \_ opción MSICOLINFO Names.

 

 



