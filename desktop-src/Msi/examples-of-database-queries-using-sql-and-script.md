---
description: En el kit de desarrollo de software (SDK) de Windows Installer se proporciona un ejemplo del uso de consultas de base de datos controladas por scripts como la utilidad WiRunSQL.vbs.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Ejemplos de consultas de base de datos mediante SQL y script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd839151b40ddd5e9a265c6c370c27a4a9fd125
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158439"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a>Ejemplos de consultas de base de datos mediante SQL y script

En el kit de desarrollo de software (SDK) de Windows [Installer](platform-sdk-components-for-windows-installer-developers.md) se proporciona un ejemplo del uso de consultas de base de datos controladas por scripts como la utilidad WiRunSQL.vbs. Esta utilidad controla las consultas de base de datos mediante la Windows installer de SQL se describe en la sección [sintaxis SQL .](sql-syntax.md)

**Eliminación de un registro de una tabla**

La siguiente línea de comandos elimina el registro que tiene la clave principal RED de la [tabla Característica](feature-table.md) de la base Test.msi datos.

**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \` Feature \` WHERE Feature \` \` . \` Característica \` ='RED'"**

**Agregar una tabla a una base de datos**

La siguiente línea de comandos agrega la [tabla Directory](directory-table.md) a la base Test.msi datos.

**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` Directory ( \` Directory \` \` CHAR(72) NOT NULL, \` Directory Parent \_ \` CHAR(72), \` DefaultDir \` CHAR(255) NOT NULL LOCALIZABLE PRIMARY KEY \` Directory \` )"**

**Eliminación de una tabla de una base de datos**

La siguiente línea de comandos quita la tabla [Feature](feature-table.md) de la base de datos Test.msi datos.

**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \` \` Feature"**

**Agregar una nueva columna a una tabla**

La siguiente línea de comandos agrega la columna Test a la [tabla CustomAction](customaction-table.md) de la base de Test.msi datos.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` CustomAction \` ADD \` Test \` INTEGER"**

**Insertar un nuevo registro en una tabla**

La siguiente línea de comandos inserta un nuevo registro en la [tabla Característica](feature-table.md) de la base Test.msi datos.

**Cscript WiRunSQL.vbs Test.msi "INSERT INTO \` Feature ( Feature \` \` \` . \` Característica \` , \` Característica \` . \` Elemento \_ primario de la característica , Característica \` \` \` . \` Title \` , \` Feature \` . \` Descripción \` , \` Característica \` . \` Mostrar \` , \` Característica \` . \` Nivel \` , \` Característica \` . \` Directorio \_ \` , Característica \` \` . \` Attributes \` ) VALUES ('Pista', 'Deportes','Pingos','Jugador',25,3,'SPORTDIR',2)"**

Esto inserta el registro siguiente en la [tabla Característica](feature-table.md) de Test.msi.

[Característica](feature-table.md) Mesa



| Característica | Elemento \_ primario de la característica | Título  | Descripción | Mostrar | Nivel | Directorio\_ | Atributos |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| Tenis  | Deporte           | Tenis | Torneo  | 25      | 3     | SPORTDIR    | 2          |



 

Tenga en cuenta que los datos binarios no se pueden insertar en una tabla directamente mediante las consultas INSERT INTO SQL UPDATE. Para obtener información, [vea Adding Binary Data to a Table Using SQL](adding-binary-data-to-a-table-using-sql.md).

**Modificación de un registro existente en una tabla**

La siguiente línea de comandos cambia el valor existente en el campo Título a "Rendimientos". El registro actualizado tiene "Ness" como clave principal y se encuentra en la tabla Feature de la base Test.msi datos.

**Cscript WiRunSQL.vbs Test.msi "UPDATE \` Feature SET Feature \` \` \` . \` Title \` ='Performances' WHERE \` Feature \` . \` Característica \` ='Sela'"**

**Selección de un grupo de registros**

La siguiente línea de comandos selecciona el nombre y el tipo de todos los controles que pertenecen a ErrorDialog en la base de Test.msi datos.

**CScript WiRunSQL.vbs Test.msi "SELECT \` Control \` , Type FROM Control WHERE Dialog \` \` \` \` \` \_ \` ='ErrorDialog' "**

**Mantener una tabla en memoria**

La siguiente línea de comandos bloquea la tabla [Component](component-table.md) de la base Test.msi base de datos en memoria.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` HOLD"**

**Liberar una tabla en memoria**

La siguiente línea de comandos libera la tabla [Component](component-table.md) de la base Test.msi base de datos de la memoria.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` FREE"**

 

 



