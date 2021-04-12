---
description: Las tablas del grupo tablas del sistema realizan un seguimiento de las tablas y columnas de la base de datos de instalación.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Grupo tablas del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482333ec3f6f483d431aced9a984c7db1ae5cef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155116"
---
# <a name="system-tables-group"></a>Grupo tablas del sistema

Las tablas del grupo tablas del sistema realizan un seguimiento de las tablas y columnas de la base de datos de instalación.

-   La [ \_ tabla tablas](-tables-table.md) realiza un seguimiento de todas las tablas de la base de datos. Esto incluye las tablas que puede haber creado para sus propias acciones personalizadas. Consulte esta tabla para averiguar si existe una tabla.
-   La [ \_ tabla de columnas](-columns-table.md) realiza un seguimiento de las columnas de la base de datos de instalación. Actualmente no se realiza el seguimiento de las columnas temporales en esta tabla. Consulte esta tabla para averiguar si existe una columna determinada.
-   En la [ \_ tabla streams](-streams-table.md) se enumeran los flujos de datos OLE incrustados.
-   La [ \_ tabla Storages](-storages-table.md) enumera los almacenamientos de datos OLE incrustados.
-   [ \_ Tabla de validación](-validation-table.md). La \_ tabla de validación realiza un seguimiento de los tipos y los intervalos permitidos de cada columna de la base de datos. La \_ tabla de validación se utiliza durante el proceso de validación de la base de datos para asegurarse de que todas las columnas se han contabilizado y tienen los valores correctos. Esta tabla no se incluye con la base de datos del instalador.

 

 



