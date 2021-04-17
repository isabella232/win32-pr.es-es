---
description: La base de datos del instalador permite al desarrollador de un paquete de instalación controlar la transferencia de una aplicación desde un origen a una imagen de destino.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Usar la base de datos del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb22b9c66547c849b4c9cbd012e78b22d9301756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677909"
---
# <a name="using-the-installer-database"></a>Usar la base de datos del instalador

La [base de datos del instalador](installer-database.md) permite al desarrollador de un paquete de instalación controlar la transferencia de una aplicación desde un origen a una imagen de destino. El diseño de las imágenes de origen y de destino de la aplicación se especifica en la tabla del [directorio](directory-table.md) y las acciones que instalan la aplicación se especifican en seis tablas de secuencia:

-   Tabla [InstallUISequence](installuisequence-table.md)
-   Tabla [InstallExecuteSequence](installexecutesequence-table.md)
-   Tabla [AdminUISequence](adminuisequence-table.md)
-   Tabla [AdminExecuteSequence](adminexecutesequence-table.md)
-   Tabla [AdvtUISequence](advtuisequence-table.md)
-   Tabla [AdvtExecuteSequence](advtexecutesequence-table.md)

En las secciones siguientes se describe cómo usar la [base de datos del instalador](installer-database.md):

-   [Usar la tabla de directorio](using-the-directory-table.md)
-   [Usar una tabla de secuencia](using-a-sequence-table.md)
-   [Obtener un identificador de base de datos](obtaining-a-database-handle.md)
-   [Confirmar bases de datos](committing-databases.md)
-   [Importar y exportar](importing-and-exporting.md)
-   [Combinar bases de datos](merging-databases.md)
-   [Asignar nombres a tablas, propiedades y acciones personalizadas](naming-custom-tables-properties-and-actions.md)
-   [Limitaciones de OLE en secuencias](ole-limitations-on-streams.md)
-   [Trabajar con consultas](working-with-queries.md)
-   [Agregar datos binarios a una tabla mediante SQL](adding-binary-data-to-a-table-using-sql.md)
-   [Trabajar con registros](working-with-records.md)
-   [Trabajar con ubicaciones de carpetas](working-with-folder-locations.md)
-   [Especificar el orden de registro automático](specifying-the-order-of-self-registration.md)
-   [Acciones de acondicionamiento que se ejecutan durante la eliminación](conditioning-actions-to-run-during-removal.md)
-   [Llamar a funciones de base de datos desde programas](calling-database-functions-from-programs.md)
-   [Sintaxis de la instrucción condicional](conditional-statement-syntax.md)
-   [Formato de definición de columna](column-definition-format.md)
-   [Determinar si una columna es una clave principal o externa](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



