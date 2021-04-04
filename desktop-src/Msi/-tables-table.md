---
description: La \_ tabla tablas es una tabla del sistema de solo lectura que enumera todas las tablas de la base de datos. Consulte esta tabla para averiguar si existe una tabla.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: _Tables tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909162"
---
# <a name="_tables-table"></a>\_Tabla tablas

La \_ tabla tablas es una tabla del sistema de solo lectura que enumera todas las tablas de la base de datos. Consulte esta tabla para averiguar si existe una tabla.

La \_ tabla tablas tiene la siguiente columna.



| Columna | Tipo             | Clave | Nullable |
|--------|------------------|-----|----------|
| Nombre   | [Texto](text.md) | Y   | N        |



 

## <a name="column"></a>Columna

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Nombre de una de las tablas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Dado que la tabla tables \_ es una tabla del sistema que no se puede modificar mediante consultas SQL, no puede obtener las claves principales con la función [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) o la [**propiedad PrimaryKeys**](database-primarykeys.md).

 

 



