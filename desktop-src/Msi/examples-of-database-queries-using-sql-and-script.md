---
description: En el kit de desarrollo de software (SDK) de Windows Installer, se proporciona un ejemplo de uso de consultas de base de datos controladas por scripts como WiRunSQL.vbs de la utilidad.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Ejemplos de consultas de base de datos mediante SQL y script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd839151b40ddd5e9a265c6c370c27a4a9fd125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812871"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a>Ejemplos de consultas de base de datos mediante SQL y script

En el [Kit de desarrollo de software](platform-sdk-components-for-windows-installer-developers.md) (SDK) de Windows Installer, se proporciona un ejemplo de uso de consultas de base de datos controladas por scripts como WiRunSQL.vbs de la utilidad. Esta utilidad controla las consultas de base de datos con la versión Windows Installer de SQL descrita en la sección [Sintaxis de SQL](sql-syntax.md).

**Eliminar un registro de una tabla**

La siguiente línea de comandos elimina el registro que tiene la clave principal en rojo de la tabla de [características](feature-table.md) de la base de datos Test.msi.

**Cscript WiRunSQL.vbs Test.msi la característica "eliminar de la \` característica \` Where \` \` . \` Característica \` = ' red ' '**

**Agregar una tabla a una base de datos**

La siguiente línea de comandos agrega la tabla del [directorio](directory-table.md) a la base de datos de Test.msi.

**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` \` ( \` directorio \` Char (72) not null, \` Directory \_ Parent \` Char (72), \` DefaultDir \` Char (255) not null PRIMARY KEY \` Directory \` )"**

**Quitar una tabla de una base de datos**

La siguiente línea de comandos quita la tabla de [características](feature-table.md) de la base de datos Test.msi.

**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \` Feature \` "**

**Agregar una nueva columna a una tabla**

La siguiente línea de comandos agrega la columna test a la tabla [CustomAction](customaction-table.md) de la base de datos Test.msi.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` CustomAction \` Add \` Test \` Integer"**

**Insertar un nuevo registro en una tabla**

La siguiente línea de comandos inserta un nuevo registro en la tabla de [características](feature-table.md) de la base de datos Test.msi.

**Cscript WiRunSQL.vbs Test.msi característica de inserción \` en \` ( \` característica) \` . \` Característica \` , \` característica \` . \` Característica \_ principal \` , \` característica \` . \` Título \` , \` característica \` . \` Descripción \` , \` característica \` . \` Mostrar \` , \` característica \` . \` Nivel \` , \` característica \` . \` Directorio \_ \` , \` característica \` . \` Valores de atributos \` (' tenis ', ' deporte ', ' tenis ', ' Torneo ', 25, 3, ' SPORTDIR ', 2) "**

Esto inserta el Registro siguiente en la tabla de [características](feature-table.md) de Test.msi.

[Característica](feature-table.md) de Cuadro



| Característica | Característica \_ principal | Title  | Descripción | Pantalla | Nivel | Directorio\_ | Atributos |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| Tenis  | Deporte           | Tenis | Torneo  | 25      | 3     | SPORTDIR    | 2          |



 

Tenga en cuenta que los datos binarios no se pueden insertar en una tabla directamente mediante las consultas INSERT INTO o UPDATE SQL. Para obtener información, consulte [Agregar datos binarios a una tabla con SQL](adding-binary-data-to-a-table-using-sql.md).

**Modificar un registro existente en una tabla**

La siguiente línea de comandos cambia el valor existente en el campo título a "rendimientos". El registro actualizado tiene "Arts" como clave principal y se encuentra en la tabla de características de la base de datos Test.msi.

**Cscript WiRunSQL.vbs Test.msi la característica de conjunto de características de actualización \` \` \` \` . \` Título \` = ' rendimiento ' en la \` característica \` . \` Feature \` = ' Arts ' "**

**Seleccionar un grupo de registros**

La siguiente línea de comandos selecciona el nombre y el tipo de todos los controles que pertenecen a ErrorDialog en la base de datos Test.msi.

**CScript WiRunSQL.vbs Test.msi "seleccionar \` control \` , \` tipo \` desde \` control \` donde \` Dialog \_ \` = ' ErrorDialog '"**

**Contener una tabla en memoria**

La siguiente línea de comandos bloquea la tabla de [componentes](component-table.md) de la base de datos Test.msi en memoria.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` Hold"**

**Liberar una tabla en memoria**

La línea de comandos siguiente libera la tabla de [componentes](component-table.md) de la base de datos Test.msi de la memoria.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` Free"**

 

 



