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
# <a name="examples-of-database-queries-using-sql-and-script"></a><span data-ttu-id="3d72d-103">Ejemplos de consultas de base de datos mediante SQL y script</span><span class="sxs-lookup"><span data-stu-id="3d72d-103">Examples of Database Queries Using SQL and Script</span></span>

<span data-ttu-id="3d72d-104">En el [Kit de desarrollo de software](platform-sdk-components-for-windows-installer-developers.md) (SDK) de Windows Installer, se proporciona un ejemplo de uso de consultas de base de datos controladas por scripts como WiRunSQL.vbs de la utilidad.</span><span class="sxs-lookup"><span data-stu-id="3d72d-104">An example of using script-driven database queries is provided in the Windows [Installer Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) as the utility WiRunSQL.vbs.</span></span> <span data-ttu-id="3d72d-105">Esta utilidad controla las consultas de base de datos con la versión Windows Installer de SQL descrita en la sección [Sintaxis de SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="3d72d-105">This utility handles database queries using the Windows Installer version of SQL described in the section [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="3d72d-106">**Eliminar un registro de una tabla**</span><span class="sxs-lookup"><span data-stu-id="3d72d-106">**Delete a record from a table**</span></span>

<span data-ttu-id="3d72d-107">La siguiente línea de comandos elimina el registro que tiene la clave principal en rojo de la tabla de [características](feature-table.md) de la base de datos Test.msi.</span><span class="sxs-lookup"><span data-stu-id="3d72d-107">The following command line deletes the record having the primary key RED from the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="3d72d-108">**Cscript WiRunSQL.vbs Test.msi la característica "eliminar de la \` característica \` Where \` \` . \` Característica \` = ' red ' '**</span><span class="sxs-lookup"><span data-stu-id="3d72d-108">**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \`Feature\` WHERE \`Feature\`.\`Feature\`='RED'"**</span></span>

<span data-ttu-id="3d72d-109">**Agregar una tabla a una base de datos**</span><span class="sxs-lookup"><span data-stu-id="3d72d-109">**Add a table to a database**</span></span>

<span data-ttu-id="3d72d-110">La siguiente línea de comandos agrega la tabla del [directorio](directory-table.md) a la base de datos de Test.msi.</span><span class="sxs-lookup"><span data-stu-id="3d72d-110">The following command line adds the [Directory](directory-table.md) table to the Test.msi database.</span></span>

<span data-ttu-id="3d72d-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` \` ( \` directorio \` Char (72) not null, \` Directory \_ Parent \` Char (72), \` DefaultDir \` Char (255) not null PRIMARY KEY \` Directory \` )"**</span><span class="sxs-lookup"><span data-stu-id="3d72d-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \`Directory\` (\`Directory\` CHAR(72) NOT NULL, \`Directory\_Parent\` CHAR(72), \`DefaultDir\` CHAR(255) NOT NULL LOCALIZABLE PRIMARY KEY \`Directory\`)"**</span></span>

<span data-ttu-id="3d72d-112">**Quitar una tabla de una base de datos**</span><span class="sxs-lookup"><span data-stu-id="3d72d-112">**Remove a table from a database**</span></span>

<span data-ttu-id="3d72d-113">La siguiente línea de comandos quita la tabla de [características](feature-table.md) de la base de datos Test.msi.</span><span class="sxs-lookup"><span data-stu-id="3d72d-113">The following command line removes the [Feature](feature-table.md) table from the Test.msi database.</span></span>

<span data-ttu-id="3d72d-114">**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \` Feature \` "**</span><span class="sxs-lookup"><span data-stu-id="3d72d-114">**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \`Feature\`"**</span></span>

<span data-ttu-id="3d72d-115">**Agregar una nueva columna a una tabla**</span><span class="sxs-lookup"><span data-stu-id="3d72d-115">**Add a new column to a table**</span></span>

<span data-ttu-id="3d72d-116">La siguiente línea de comandos agrega la columna test a la tabla [CustomAction](customaction-table.md) de la base de datos Test.msi.</span><span class="sxs-lookup"><span data-stu-id="3d72d-116">The following command line adds the Test column to the [CustomAction](customaction-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="3d72d-117">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` CustomAction \` Add \` Test \` Integer"**</span><span class="sxs-lookup"><span data-stu-id="3d72d-117">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`CustomAction\` ADD \`Test\` INTEGER"**</span></span>

<span data-ttu-id="3d72d-118">**Insertar un nuevo registro en una tabla**</span><span class="sxs-lookup"><span data-stu-id="3d72d-118">**Insert a new record into a table**</span></span>

<span data-ttu-id="3d72d-119">La siguiente línea de comandos inserta un nuevo registro en la tabla de [características](feature-table.md) de la base de datos Test.msi.</span><span class="sxs-lookup"><span data-stu-id="3d72d-119">The following command line inserts a new record into the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="3d72d-120">**Cscript WiRunSQL.vbs Test.msi característica de inserción \` en \` ( \` característica) \` . \` Característica \` , \` característica \` . \` Característica \_ principal \` , \` característica \` . \` Título \` , \` característica \` . \` Descripción \` , \` característica \` . \` Mostrar \` , \` característica \` . \` Nivel \` , \` característica \` . \` Directorio \_ \` , \` característica \` . \` Valores de atributos \` (' tenis ', ' deporte ', ' tenis ', ' Torneo ', 25, 3, ' SPORTDIR ', 2) "**</span><span class="sxs-lookup"><span data-stu-id="3d72d-120">**Cscript WiRunSQL.vbs Test.msi "INSERT INTO \`Feature\` (\`Feature\`.\`Feature\`,\`Feature\`.\`Feature\_Parent\`,\`Feature\`.\`Title\`,\`Feature\`.\`Description\`, \`Feature\`.\`Display\`,\`Feature\`.\`Level\`,\`Feature\`.\`Directory\_\`,\`Feature\`.\`Attributes\`) VALUES ('Tennis','Sport','Tennis','Tournament',25,3,'SPORTDIR',2)"**</span></span>

<span data-ttu-id="3d72d-121">Esto inserta el Registro siguiente en la tabla de [características](feature-table.md) de Test.msi.</span><span class="sxs-lookup"><span data-stu-id="3d72d-121">This inserts the following record into the [Feature](feature-table.md) table of Test.msi.</span></span>

<span data-ttu-id="3d72d-122">[Característica](feature-table.md) de Cuadro</span><span class="sxs-lookup"><span data-stu-id="3d72d-122">[Feature](feature-table.md) Table</span></span>



| <span data-ttu-id="3d72d-123">Característica</span><span class="sxs-lookup"><span data-stu-id="3d72d-123">Feature</span></span> | <span data-ttu-id="3d72d-124">Característica \_ principal</span><span class="sxs-lookup"><span data-stu-id="3d72d-124">Feature\_Parent</span></span> | <span data-ttu-id="3d72d-125">Title</span><span class="sxs-lookup"><span data-stu-id="3d72d-125">Title</span></span>  | <span data-ttu-id="3d72d-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d72d-126">Description</span></span> | <span data-ttu-id="3d72d-127">Pantalla</span><span class="sxs-lookup"><span data-stu-id="3d72d-127">Display</span></span> | <span data-ttu-id="3d72d-128">Nivel</span><span class="sxs-lookup"><span data-stu-id="3d72d-128">Level</span></span> | <span data-ttu-id="3d72d-129">Directorio\_</span><span class="sxs-lookup"><span data-stu-id="3d72d-129">Directory\_</span></span> | <span data-ttu-id="3d72d-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="3d72d-130">Attributes</span></span> |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| <span data-ttu-id="3d72d-131">Tenis</span><span class="sxs-lookup"><span data-stu-id="3d72d-131">Tennis</span></span>  | <span data-ttu-id="3d72d-132">Deporte</span><span class="sxs-lookup"><span data-stu-id="3d72d-132">Sport</span></span>           | <span data-ttu-id="3d72d-133">Tenis</span><span class="sxs-lookup"><span data-stu-id="3d72d-133">Tennis</span></span> | <span data-ttu-id="3d72d-134">Torneo</span><span class="sxs-lookup"><span data-stu-id="3d72d-134">Tournament</span></span>  | <span data-ttu-id="3d72d-135">25</span><span class="sxs-lookup"><span data-stu-id="3d72d-135">25</span></span>      | <span data-ttu-id="3d72d-136">3</span><span class="sxs-lookup"><span data-stu-id="3d72d-136">3</span></span>     | <span data-ttu-id="3d72d-137">SPORTDIR</span><span class="sxs-lookup"><span data-stu-id="3d72d-137">SPORTDIR</span></span>    | <span data-ttu-id="3d72d-138">2</span><span class="sxs-lookup"><span data-stu-id="3d72d-138">2</span></span>          |



 

<span data-ttu-id="3d72d-139">Tenga en cuenta que los datos binarios no se pueden insertar en una tabla directamente mediante las consultas INSERT INTO o UPDATE SQL.</span><span class="sxs-lookup"><span data-stu-id="3d72d-139">Note that binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL queries.</span></span> <span data-ttu-id="3d72d-140">Para obtener información, consulte [Agregar datos binarios a una tabla con SQL](adding-binary-data-to-a-table-using-sql.md).</span><span class="sxs-lookup"><span data-stu-id="3d72d-140">For information see [Adding Binary Data to a Table Using SQL](adding-binary-data-to-a-table-using-sql.md).</span></span>

<span data-ttu-id="3d72d-141">**Modificar un registro existente en una tabla**</span><span class="sxs-lookup"><span data-stu-id="3d72d-141">**Modify an existing record in a table**</span></span>

<span data-ttu-id="3d72d-142">La siguiente línea de comandos cambia el valor existente en el campo título a "rendimientos".</span><span class="sxs-lookup"><span data-stu-id="3d72d-142">The following command line changes the existing value in the Title field to "Performances."</span></span> <span data-ttu-id="3d72d-143">El registro actualizado tiene "Arts" como clave principal y se encuentra en la tabla de características de la base de datos Test.msi.</span><span class="sxs-lookup"><span data-stu-id="3d72d-143">The updated record has "Arts" as its primary key and is in the Feature table of the Test.msi database.</span></span>

<span data-ttu-id="3d72d-144">**Cscript WiRunSQL.vbs Test.msi la característica de conjunto de características de actualización \` \` \` \` . \` Título \` = ' rendimiento ' en la \` característica \` . \` Feature \` = ' Arts ' "**</span><span class="sxs-lookup"><span data-stu-id="3d72d-144">**Cscript WiRunSQL.vbs Test.msi "UPDATE \`Feature\` SET \`Feature\`.\`Title\`='Performances' WHERE \`Feature\`.\`Feature\`='Arts'"**</span></span>

<span data-ttu-id="3d72d-145">**Seleccionar un grupo de registros**</span><span class="sxs-lookup"><span data-stu-id="3d72d-145">**Select a group of records**</span></span>

<span data-ttu-id="3d72d-146">La siguiente línea de comandos selecciona el nombre y el tipo de todos los controles que pertenecen a ErrorDialog en la base de datos Test.msi.</span><span class="sxs-lookup"><span data-stu-id="3d72d-146">The following command line selects the name and type of all controls that belong to the ErrorDialog in the Test.msi database.</span></span>

<span data-ttu-id="3d72d-147">**CScript WiRunSQL.vbs Test.msi "seleccionar \` control \` , \` tipo \` desde \` control \` donde \` Dialog \_ \` = ' ErrorDialog '"**</span><span class="sxs-lookup"><span data-stu-id="3d72d-147">**CScript WiRunSQL.vbs Test.msi "SELECT \`Control\`, \`Type\` FROM \`Control\` WHERE \`Dialog\_\`='ErrorDialog' "**</span></span>

<span data-ttu-id="3d72d-148">**Contener una tabla en memoria**</span><span class="sxs-lookup"><span data-stu-id="3d72d-148">**Hold a table in memory**</span></span>

<span data-ttu-id="3d72d-149">La siguiente línea de comandos bloquea la tabla de [componentes](component-table.md) de la base de datos Test.msi en memoria.</span><span class="sxs-lookup"><span data-stu-id="3d72d-149">The following command line locks the [Component](component-table.md) table of the Test.msi database in memory.</span></span>

<span data-ttu-id="3d72d-150">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` Hold"**</span><span class="sxs-lookup"><span data-stu-id="3d72d-150">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` HOLD"**</span></span>

<span data-ttu-id="3d72d-151">**Liberar una tabla en memoria**</span><span class="sxs-lookup"><span data-stu-id="3d72d-151">**Free a table in memory**</span></span>

<span data-ttu-id="3d72d-152">La línea de comandos siguiente libera la tabla de [componentes](component-table.md) de la base de datos Test.msi de la memoria.</span><span class="sxs-lookup"><span data-stu-id="3d72d-152">The following command line frees the [Component](component-table.md) table of the Test.msi database from memory.</span></span>

<span data-ttu-id="3d72d-153">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` Free"**</span><span class="sxs-lookup"><span data-stu-id="3d72d-153">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` FREE"**</span></span>

 

 



