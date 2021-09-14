---
description: Las tablas del grupo de tablas del sistema realiza un seguimiento de las tablas y columnas de la base de datos de instalación.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Grupo de tablas del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482333ec3f6f483d431aced9a984c7db1ae5cef4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069633"
---
# <a name="system-tables-group"></a>Grupo de tablas del sistema

Las tablas del grupo de tablas del sistema realiza un seguimiento de las tablas y columnas de la base de datos de instalación.

-   La [ \_ tabla Tablas realiza un](-tables-table.md) seguimiento de todas las tablas de la base de datos. Esto incluye las tablas que puede haber creado para sus propias acciones personalizadas. Consulte esta tabla para averiguar si existe una tabla.
-   La [ \_ tabla Columnas realiza un](-columns-table.md) seguimiento de las columnas de la base de datos de instalación. Actualmente, esta tabla no realiza el seguimiento de las columnas temporales. Consulte esta tabla para averiguar si existe una columna determinada.
-   La [ \_ Secuencias enumera](-streams-table.md) los flujos de datos OLE incrustados.
-   En [ \_ la tabla Storages se enumeran](-storages-table.md) los almacenamientos de datos OLE incrustados.
-   La [ \_ tabla Validation](-validation-table.md). La \_ tabla Validación realiza un seguimiento de los tipos y los intervalos permitidos de cada columna de la base de datos. La tabla Validación se usa durante el proceso de validación de la base de datos para asegurarse de que todas las columnas se tienen en cuenta y \_ tienen los valores correctos. Esta tabla no se incluye con la base de datos del instalador.

 

 



