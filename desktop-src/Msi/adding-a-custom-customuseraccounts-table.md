---
description: Una especificación del ejemplo es que la información de la cuenta de usuario se lee de una tabla personalizada en la base de datos de instalación y no se codifica de forma rígida en la acción personalizada.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Agregar una tabla CustomUserAccounts personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652629"
---
# <a name="adding-a-custom-customuseraccounts-table"></a><span data-ttu-id="a8ede-103">Agregar una tabla CustomUserAccounts personalizada</span><span class="sxs-lookup"><span data-stu-id="a8ede-103">Adding a Custom CustomUserAccounts Table</span></span>

<span data-ttu-id="a8ede-104">Una especificación del ejemplo es que la información de la cuenta de usuario se lee de una tabla personalizada en la base de datos de instalación y no se codifica de forma rígida en la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="a8ede-104">A specification of the sample is that user account information be read from a custom table in the installation database and not hard-coded into the custom action.</span></span>

<span data-ttu-id="a8ede-105">Agregue una tabla personalizada a la base de datos de instalación de ejemplo denominada CustomUserAccounts para almacenar la información de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="a8ede-105">Add a custom table to the sample installation database named CustomUserAccounts to hold user account information.</span></span> <span data-ttu-id="a8ede-106">Vea [ejemplos de consultas de base de datos mediante SQL y script](examples-of-database-queries-using-sql-and-script.md) para obtener un ejemplo de cómo agregar una tabla personalizada.</span><span class="sxs-lookup"><span data-stu-id="a8ede-106">See [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md) for an example of how to add a custom table.</span></span> <span data-ttu-id="a8ede-107">Use el siguiente esquema para la tabla CustomUserAccounts.</span><span class="sxs-lookup"><span data-stu-id="a8ede-107">Use the following schema for the CustomUserAccounts table.</span></span> <span data-ttu-id="a8ede-108">Vea [formato de definición de columna](column-definition-format.md) para obtener una explicación de los tipos de columna.</span><span class="sxs-lookup"><span data-stu-id="a8ede-108">See [Column Definition Format](column-definition-format.md) for an explanation of the column types.</span></span>



| <span data-ttu-id="a8ede-109">Columna</span><span class="sxs-lookup"><span data-stu-id="a8ede-109">Column</span></span>     | <span data-ttu-id="a8ede-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8ede-110">Type</span></span> | <span data-ttu-id="a8ede-111">Clave</span><span class="sxs-lookup"><span data-stu-id="a8ede-111">Key</span></span> | <span data-ttu-id="a8ede-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="a8ede-112">Nullable</span></span> | <span data-ttu-id="a8ede-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8ede-113">Description</span></span>                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ede-114">UserName</span><span class="sxs-lookup"><span data-stu-id="a8ede-114">UserName</span></span>   | <span data-ttu-id="a8ede-115">S72</span><span class="sxs-lookup"><span data-stu-id="a8ede-115">s72</span></span>  | <span data-ttu-id="a8ede-116">Y</span><span class="sxs-lookup"><span data-stu-id="a8ede-116">Y</span></span>   | <span data-ttu-id="a8ede-117">N</span><span class="sxs-lookup"><span data-stu-id="a8ede-117">N</span></span>        | <span data-ttu-id="a8ede-118">Nombre de la cuenta de usuario que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="a8ede-118">Name of user account being created.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a8ede-119">Contraseña</span><span class="sxs-lookup"><span data-stu-id="a8ede-119">Password</span></span>   | <span data-ttu-id="a8ede-120">S72</span><span class="sxs-lookup"><span data-stu-id="a8ede-120">s72</span></span>  |     | <span data-ttu-id="a8ede-121">N</span><span class="sxs-lookup"><span data-stu-id="a8ede-121">N</span></span>        | <span data-ttu-id="a8ede-122">Nombre de la propiedad que contiene la contraseña de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="a8ede-122">Name of property containing the password for the account.</span></span> <span data-ttu-id="a8ede-123">Se trata de una [propiedad pública](public-properties.md) establecida en la línea de comandos o a través de un [control de edición](edit-control.md) en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a8ede-123">This is a [public property](public-properties.md) set on the command line or through an [edit control](edit-control.md) in the user interface.</span></span> <span data-ttu-id="a8ede-124">Este control de edición debe tener el [atributo de control de contraseña](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="a8ede-124">This edit control should have the [Password Control Attribute](password-control-attribute.md).</span></span> |
| <span data-ttu-id="a8ede-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8ede-125">Attributes</span></span> | <span data-ttu-id="a8ede-126">i4</span><span class="sxs-lookup"><span data-stu-id="a8ede-126">i4</span></span>   |     | <span data-ttu-id="a8ede-127">Y</span><span class="sxs-lookup"><span data-stu-id="a8ede-127">Y</span></span>        | <span data-ttu-id="a8ede-128">Atributos de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="a8ede-128">Attributes for account.</span></span> <span data-ttu-id="a8ede-129">Se definen como valores **DWORD** para el \_ miembro usri1 flags de la estructura de \_ información de usuario \_ 1.</span><span class="sxs-lookup"><span data-stu-id="a8ede-129">These are defined as the **DWORD** values for the usri1\_flags member of the USER\_INFO\_1 structure.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="a8ede-130">Una vez agregada la tabla CustomUserAccounts a la base de datos, puede editar esta tabla mediante orca, un editor de tablas proporcionado con el SDK de Windows Installer u otro editor.</span><span class="sxs-lookup"><span data-stu-id="a8ede-130">After the CustomUserAccounts table has been added to the database you may edit this table using Orca, a table editor provided with the Windows Installer SDK, or another editor.</span></span> <span data-ttu-id="a8ede-131">Escriba el Registro siguiente en la tabla CustomUserAccounts para crear una cuenta de usuario protegida con contraseña para un usuario llamado TestUser.</span><span class="sxs-lookup"><span data-stu-id="a8ede-131">Enter the following record in the CustomUserAccounts table to create a password secured user account for a user called TestUser.</span></span> <span data-ttu-id="a8ede-132">Tenga en cuenta que 512 es el valor numérico de la cuenta de fi \_ normal \_ .</span><span class="sxs-lookup"><span data-stu-id="a8ede-132">Note that 512 is the numeric value for UF\_NORMAL\_ACCOUNT.</span></span>

<span data-ttu-id="a8ede-133">Tabla CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="a8ede-133">CustomUserAccounts Table</span></span>



| <span data-ttu-id="a8ede-134">UserName</span><span class="sxs-lookup"><span data-stu-id="a8ede-134">UserName</span></span> | <span data-ttu-id="a8ede-135">Contraseña</span><span class="sxs-lookup"><span data-stu-id="a8ede-135">Password</span></span>         | <span data-ttu-id="a8ede-136">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8ede-136">Attributes</span></span> |
|----------|------------------|------------|
| <span data-ttu-id="a8ede-137">TestUser</span><span class="sxs-lookup"><span data-stu-id="a8ede-137">TestUser</span></span> | <span data-ttu-id="a8ede-138">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="a8ede-138">TESTUSERPASSWORD</span></span> | <span data-ttu-id="a8ede-139">512</span><span class="sxs-lookup"><span data-stu-id="a8ede-139">512</span></span>        |



 

<span data-ttu-id="a8ede-140">Agregue los siguientes registros a la \_ tabla de validación para la tabla personalizada.</span><span class="sxs-lookup"><span data-stu-id="a8ede-140">Add the following records to the \_Validation table for the custom table.</span></span>

[<span data-ttu-id="a8ede-141">\_Tabla de validación</span><span class="sxs-lookup"><span data-stu-id="a8ede-141">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="a8ede-142">Tabla</span><span class="sxs-lookup"><span data-stu-id="a8ede-142">Table</span></span>              | <span data-ttu-id="a8ede-143">Columna</span><span class="sxs-lookup"><span data-stu-id="a8ede-143">Column</span></span>     | <span data-ttu-id="a8ede-144">Nullable</span><span class="sxs-lookup"><span data-stu-id="a8ede-144">Nullable</span></span> | <span data-ttu-id="a8ede-145">MinValue</span><span class="sxs-lookup"><span data-stu-id="a8ede-145">MinValue</span></span> | <span data-ttu-id="a8ede-146">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a8ede-146">MaxValue</span></span>   | <span data-ttu-id="a8ede-147">KeyTable</span><span class="sxs-lookup"><span data-stu-id="a8ede-147">KeyTable</span></span> | <span data-ttu-id="a8ede-148">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="a8ede-148">KeyColumn</span></span> | <span data-ttu-id="a8ede-149">Category</span><span class="sxs-lookup"><span data-stu-id="a8ede-149">Category</span></span>                     | <span data-ttu-id="a8ede-150">Set</span><span class="sxs-lookup"><span data-stu-id="a8ede-150">Set</span></span> | <span data-ttu-id="a8ede-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8ede-151">Description</span></span> |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| <span data-ttu-id="a8ede-152">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="a8ede-152">CustomUserAccounts</span></span> | <span data-ttu-id="a8ede-153">UserName</span><span class="sxs-lookup"><span data-stu-id="a8ede-153">UserName</span></span>   | <span data-ttu-id="a8ede-154">N</span><span class="sxs-lookup"><span data-stu-id="a8ede-154">N</span></span>        |          |            |          |           | [<span data-ttu-id="a8ede-155">Texto</span><span class="sxs-lookup"><span data-stu-id="a8ede-155">Text</span></span>](text.md)             |     |             |
| <span data-ttu-id="a8ede-156">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="a8ede-156">CustomUserAccounts</span></span> | <span data-ttu-id="a8ede-157">Contraseña</span><span class="sxs-lookup"><span data-stu-id="a8ede-157">Password</span></span>   | <span data-ttu-id="a8ede-158">N</span><span class="sxs-lookup"><span data-stu-id="a8ede-158">N</span></span>        |          |            |          |           | [<span data-ttu-id="a8ede-159">Identificador</span><span class="sxs-lookup"><span data-stu-id="a8ede-159">Identifier</span></span>](identifier.md) |     |             |
| <span data-ttu-id="a8ede-160">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="a8ede-160">CustomUserAccounts</span></span> | <span data-ttu-id="a8ede-161">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8ede-161">Attributes</span></span> | <span data-ttu-id="a8ede-162">Y</span><span class="sxs-lookup"><span data-stu-id="a8ede-162">Y</span></span>        | <span data-ttu-id="a8ede-163">0</span><span class="sxs-lookup"><span data-stu-id="a8ede-163">0</span></span>        | <span data-ttu-id="a8ede-164">2147483647</span><span class="sxs-lookup"><span data-stu-id="a8ede-164">2147483647</span></span> |          |           | <span data-ttu-id="a8ede-165">null</span><span class="sxs-lookup"><span data-stu-id="a8ede-165">null</span></span>                         |     |             |



 

<span data-ttu-id="a8ede-166">Continúe con [la creación de las tablas de error y de ActionText](authoring-the-actiontext-and-error-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a8ede-166">Continue to [Authoring the ActionText and Error Tables](authoring-the-actiontext-and-error-tables.md).</span></span>

 

 



