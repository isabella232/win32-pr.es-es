---
description: La \_ tabla Tablas es una tabla del sistema de solo lectura que enumera todas las tablas de la base de datos. Consulte esta tabla para averiguar si existe una tabla.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: _Tables tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c251693d89bb23634b222518e98dba270856e672362bcdc9acddd3c0b86c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013323"
---
# <a name="_tables-table"></a>\_Tabla de tablas

La \_ tabla Tablas es una tabla del sistema de solo lectura que enumera todas las tablas de la base de datos. Consulte esta tabla para averiguar si existe una tabla.

La \_ Tabla de tablas tiene la columna siguiente.



| Columna | Tipo             | Clave | Nullable |
|--------|------------------|-----|----------|
| Nombre   | [Texto](text.md) | Y   | N        |



 

## <a name="column"></a>Columna

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Nombre de una de las tablas.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Dado que la tabla Tables es una tabla del sistema que no se puede modificar mediante consultas SQL, no se pueden obtener las claves principales con la función \_ [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) o la [**propiedad PrimaryKeys**](database-primarykeys.md).

 

 



