---
description: Las tablas del grupo de tablas del sistema realiza un seguimiento de las tablas y columnas de la base de datos de instalación.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Grupo de tablas del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c05bfd06bcff049d2aea847a2bb8d0c4c3fc3d1443a615f75912ac7d4f86d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623924"
---
# <a name="system-tables-group"></a>Grupo de tablas del sistema

Las tablas del grupo de tablas del sistema realiza un seguimiento de las tablas y columnas de la base de datos de instalación.

-   La [ \_ tabla Tablas realiza un](-tables-table.md) seguimiento de todas las tablas de la base de datos. Esto incluye las tablas que puede haber creado para sus propias acciones personalizadas. Consulte esta tabla para averiguar si existe una tabla.
-   La [ \_ tabla Columnas realiza un seguimiento](-columns-table.md) de las columnas de la base de datos de instalación. Actualmente, esta tabla no realiza el seguimiento de las columnas temporales. Consulte esta tabla para averiguar si existe una columna determinada.
-   La [ \_ Secuencias enumera los](-streams-table.md) flujos de datos OLE incrustados.
-   En [ \_ la tabla Storages se enumeran](-storages-table.md) los almacenamientos de datos OLE incrustados.
-   La [ \_ tabla Validation](-validation-table.md). La \_ tabla Validation realiza un seguimiento de los tipos y los intervalos permitidos de cada columna de la base de datos. La tabla Validation se usa durante el proceso de validación de la base de datos para asegurarse de que todas las columnas se tienen en cuenta \_ y tienen los valores correctos. Esta tabla no se incluye con la base de datos del instalador.

 

 



