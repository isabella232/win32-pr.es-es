---
description: MsiViewGetColumnInfo y la propiedad ColumnInfo del objeto View usan el siguiente formato para describir las definiciones de las columnas de la base de datos.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Formato de definición de columna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277187"
---
# <a name="column-definition-format"></a><span data-ttu-id="e0d14-103">Formato de definición de columna</span><span class="sxs-lookup"><span data-stu-id="e0d14-103">Column Definition Format</span></span>

<span data-ttu-id="e0d14-104">[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) y la [**propiedad ColumnInfo**](view-columninfo.md) del objeto [**View**](view-object.md) usan el siguiente formato para describir las definiciones de las columnas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e0d14-104">[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) and the [**ColumnInfo Property**](view-columninfo.md) of the [**View**](view-object.md) object use the following format to describe database column definitions.</span></span> <span data-ttu-id="e0d14-105">Cada columna se describe mediante una cadena en el campo registro correspondiente devuelto por la función o la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e0d14-105">Each column is described by a string in the corresponding record field returned by the function or property.</span></span> <span data-ttu-id="e0d14-106">La cadena de definición se compone de una sola letra que representa el tipo de datos seguido del ancho de la columna (en caracteres, si es aplicable, bytes de lo contrario).</span><span class="sxs-lookup"><span data-stu-id="e0d14-106">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, bytes otherwise).</span></span> <span data-ttu-id="e0d14-107">Un ancho de cero designa un ancho sin enlazar (por ejemplo, campos de texto largo y secuencias).</span><span class="sxs-lookup"><span data-stu-id="e0d14-107">A width of zero designates an unbounded width (for example, long text fields and streams).</span></span> <span data-ttu-id="e0d14-108">Una letra mayúscula indica que se permiten valores NULL en la columna.</span><span class="sxs-lookup"><span data-stu-id="e0d14-108">An uppercase letter indicates that null values are allowed in the column.</span></span>



| <span data-ttu-id="e0d14-109">Descriptor de columna</span><span class="sxs-lookup"><span data-stu-id="e0d14-109">Column descriptor</span></span> | <span data-ttu-id="e0d14-110">Cadena de definición</span><span class="sxs-lookup"><span data-stu-id="e0d14-110">Definition string</span></span>                 |
|-------------------|-----------------------------------|
| <span data-ttu-id="e0d14-111">seg?</span><span class="sxs-lookup"><span data-stu-id="e0d14-111">s?</span></span>                | <span data-ttu-id="e0d14-112">Cadena, longitud variable (? = 1-255)</span><span class="sxs-lookup"><span data-stu-id="e0d14-112">String, variable length (?=1-255)</span></span> |
| <span data-ttu-id="e0d14-113">S0</span><span class="sxs-lookup"><span data-stu-id="e0d14-113">s0</span></span>                | <span data-ttu-id="e0d14-114">Cadena, longitud variable</span><span class="sxs-lookup"><span data-stu-id="e0d14-114">String, variable length</span></span>           |
| <span data-ttu-id="e0d14-115">i2</span><span class="sxs-lookup"><span data-stu-id="e0d14-115">i2</span></span>                | <span data-ttu-id="e0d14-116">Entero corto</span><span class="sxs-lookup"><span data-stu-id="e0d14-116">Short integer</span></span>                     |
| <span data-ttu-id="e0d14-117">i4</span><span class="sxs-lookup"><span data-stu-id="e0d14-117">i4</span></span>                | <span data-ttu-id="e0d14-118">Entero largo</span><span class="sxs-lookup"><span data-stu-id="e0d14-118">Long integer</span></span>                      |
| <span data-ttu-id="e0d14-119">v0</span><span class="sxs-lookup"><span data-stu-id="e0d14-119">v0</span></span>                | <span data-ttu-id="e0d14-120">Secuencia binaria</span><span class="sxs-lookup"><span data-stu-id="e0d14-120">Binary Stream</span></span>                     |
| <span data-ttu-id="e0d14-121">i?</span><span class="sxs-lookup"><span data-stu-id="e0d14-121">g?</span></span>                | <span data-ttu-id="e0d14-122">Cadena temporal (? = 0-255)</span><span class="sxs-lookup"><span data-stu-id="e0d14-122">Temporary string (?=0-255)</span></span>        |
| <span data-ttu-id="e0d14-123">j?</span><span class="sxs-lookup"><span data-stu-id="e0d14-123">j?</span></span>                | <span data-ttu-id="e0d14-124">Entero temporal (? = 0, 1, 2, 4)</span><span class="sxs-lookup"><span data-stu-id="e0d14-124">Temporary integer (?=0,1,2,4)</span></span>     |
| <span data-ttu-id="e0d14-125">O0</span><span class="sxs-lookup"><span data-stu-id="e0d14-125">O0</span></span>                | <span data-ttu-id="e0d14-126">Objeto temporal</span><span class="sxs-lookup"><span data-stu-id="e0d14-126">Temporary object</span></span>                  |



 

<span data-ttu-id="e0d14-127">Las cadenas usadas para describir columnas tienen la relación siguiente con las cadenas de consulta SQL utilizadas por CREATE y ALTER.</span><span class="sxs-lookup"><span data-stu-id="e0d14-127">The strings used to describe columns have the following relationship to the SQL query strings used by CREATE and ALTER.</span></span> <span data-ttu-id="e0d14-128">Para obtener más información, vea [Sintaxis de SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e0d14-128">For more information, see [SQL Syntax](sql-syntax.md).</span></span>



| <span data-ttu-id="e0d14-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0d14-129">Returned value</span></span> | <span data-ttu-id="e0d14-130">Sintaxis de SQL</span><span class="sxs-lookup"><span data-stu-id="e0d14-130">SQL syntax</span></span>                |
|----------------|---------------------------|
| <span data-ttu-id="e0d14-131">S0</span><span class="sxs-lookup"><span data-stu-id="e0d14-131">s0</span></span>             | <span data-ttu-id="e0d14-132">LONGCHAR</span><span class="sxs-lookup"><span data-stu-id="e0d14-132">LONGCHAR</span></span>                  |
| <span data-ttu-id="e0d14-133">L0</span><span class="sxs-lookup"><span data-stu-id="e0d14-133">l0</span></span>             | <span data-ttu-id="e0d14-134">LONGCHAR LOCALIZABLE</span><span class="sxs-lookup"><span data-stu-id="e0d14-134">LONGCHAR LOCALIZABLE</span></span>      |
| <span data-ttu-id="e0d14-135">seg \#</span><span class="sxs-lookup"><span data-stu-id="e0d14-135">s \#</span></span>           | <span data-ttu-id="e0d14-136">CHAR ( \# )</span><span class="sxs-lookup"><span data-stu-id="e0d14-136">CHAR(\#)</span></span>                  |
| <span data-ttu-id="e0d14-137">seg \#</span><span class="sxs-lookup"><span data-stu-id="e0d14-137">s \#</span></span>           | <span data-ttu-id="e0d14-138">CARÁCTER ( \# )</span><span class="sxs-lookup"><span data-stu-id="e0d14-138">CHARACTER(\#)</span></span>             |
| <span data-ttu-id="e0d14-139">CG \#</span><span class="sxs-lookup"><span data-stu-id="e0d14-139">l \#</span></span>           | <span data-ttu-id="e0d14-140">CHAR ( \# ) traducible</span><span class="sxs-lookup"><span data-stu-id="e0d14-140">CHAR(\#) LOCALIZABLE</span></span>      |
| <span data-ttu-id="e0d14-141">CG \#</span><span class="sxs-lookup"><span data-stu-id="e0d14-141">l \#</span></span>           | <span data-ttu-id="e0d14-142">CARÁCTER ( \# ) localizable</span><span class="sxs-lookup"><span data-stu-id="e0d14-142">CHARACTER(\#) LOCALIZABLE</span></span> |
| <span data-ttu-id="e0d14-143">i2</span><span class="sxs-lookup"><span data-stu-id="e0d14-143">i2</span></span>             | <span data-ttu-id="e0d14-144">SHORT</span><span class="sxs-lookup"><span data-stu-id="e0d14-144">SHORT</span></span>                     |
| <span data-ttu-id="e0d14-145">i2</span><span class="sxs-lookup"><span data-stu-id="e0d14-145">i2</span></span>             | <span data-ttu-id="e0d14-146">INT</span><span class="sxs-lookup"><span data-stu-id="e0d14-146">INT</span></span>                       |
| <span data-ttu-id="e0d14-147">i2</span><span class="sxs-lookup"><span data-stu-id="e0d14-147">i2</span></span>             | <span data-ttu-id="e0d14-148">INTEGER</span><span class="sxs-lookup"><span data-stu-id="e0d14-148">INTEGER</span></span>                   |
| <span data-ttu-id="e0d14-149">i4</span><span class="sxs-lookup"><span data-stu-id="e0d14-149">i4</span></span>             | <span data-ttu-id="e0d14-150">LONG</span><span class="sxs-lookup"><span data-stu-id="e0d14-150">LONG</span></span>                      |
| <span data-ttu-id="e0d14-151">v0</span><span class="sxs-lookup"><span data-stu-id="e0d14-151">v0</span></span>             | <span data-ttu-id="e0d14-152">OBJECT</span><span class="sxs-lookup"><span data-stu-id="e0d14-152">OBJECT</span></span>                    |



 

<span data-ttu-id="e0d14-153">Si la letra no se escribe en mayúsculas, la instrucción SQL debe anexarse con NOT NULL.</span><span class="sxs-lookup"><span data-stu-id="e0d14-153">If the letter is not capitalized, the SQL statement should be appended with NOT NULL.</span></span>



| <span data-ttu-id="e0d14-154">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0d14-154">Returned value</span></span> | <span data-ttu-id="e0d14-155">Sintaxis de SQL</span><span class="sxs-lookup"><span data-stu-id="e0d14-155">SQL syntax</span></span>        |
|----------------|-------------------|
| <span data-ttu-id="e0d14-156">S0</span><span class="sxs-lookup"><span data-stu-id="e0d14-156">s0</span></span>             | <span data-ttu-id="e0d14-157">LONGCHAR NOT NULL</span><span class="sxs-lookup"><span data-stu-id="e0d14-157">LONGCHAR NOT NULL</span></span> |



 

<span data-ttu-id="e0d14-158">El instalador no limita internamente la longitud de las columnas al valor especificado por el formato de definición de columna.</span><span class="sxs-lookup"><span data-stu-id="e0d14-158">The installer does not internally limit the length of columns to the value specified by the column definition format.</span></span> <span data-ttu-id="e0d14-159">Si los datos introducidos en un campo superan la longitud de columna especificada, el paquete no supera la [validación del paquete](package-validation.md).</span><span class="sxs-lookup"><span data-stu-id="e0d14-159">If the data entered into a field exceeds the specified column length, the package fails to pass [package validation](package-validation.md).</span></span> <span data-ttu-id="e0d14-160">Para pasar la validación en este caso, se deben cambiar los datos o el esquema de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e0d14-160">To pass validation in this case, either the data or the database schema must be changed.</span></span> <span data-ttu-id="e0d14-161">La única forma de cambiar la longitud de la columna de una tabla estándar es exportando la tabla mediante [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), editando el archivo. IDT exportado y, a continuación, importando la tabla con [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="e0d14-161">The only means to change the column length of a standard table is by exporting the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), editing the exported .idt file, and then importing the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="e0d14-162">Los autores no pueden cambiar los tipos de datos de columna, la nulabilidad o los atributos de localización de las columnas de las tablas estándar.</span><span class="sxs-lookup"><span data-stu-id="e0d14-162">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="e0d14-163">Los autores pueden crear tablas personalizadas con columnas que tengan atributos de columna.</span><span class="sxs-lookup"><span data-stu-id="e0d14-163">Authors can create custom tables with columns having any column attributes.</span></span>

<span data-ttu-id="e0d14-164">Al usar [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) para combinar una base de datos de referencia en una base de datos de destino, los nombres de columna, el número de claves principales y los tipos de datos de columna deben coincidir.</span><span class="sxs-lookup"><span data-stu-id="e0d14-164">When using [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to merge a reference database into a target database, the column names, number of primary keys, and column data types must match.</span></span> <span data-ttu-id="e0d14-165">**MsiDatabaseMerge** omite los atributos de localización y de longitud de columna.</span><span class="sxs-lookup"><span data-stu-id="e0d14-165">**MsiDatabaseMerge** ignores the localization and column length attributes.</span></span> <span data-ttu-id="e0d14-166">Si una columna de la base de datos de referencia tiene una longitud que es 0 o mayor que la longitud de la columna en la base de datos de destino, **MsiDatabaseMerge** aumenta la longitud de la columna en la base de datos de destino a la longitud de la base de datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="e0d14-166">If a column in the reference database has a length that is 0 or greater than the that column's length in the target database, **MsiDatabaseMerge** increases the column length in the target database to the length in the reference database.</span></span>

<span data-ttu-id="e0d14-167">Cuando se usa Mergmod.dll versión 2,0, la aplicación de un módulo de combinación a un archivo. msi nunca cambia la longitud de las columnas o los tipos de columna de una tabla de base de datos existente.</span><span class="sxs-lookup"><span data-stu-id="e0d14-167">When using Mergmod.dll version 2.0, the application of a merge module to a .msi file never changes the length of columns or the column types of an existing database table.</span></span> <span data-ttu-id="e0d14-168">Sin embargo, la aplicación de un módulo de combinación puede cambiar el esquema de una tabla de base de datos existente si el módulo agrega nuevas columnas a una tabla para la que es válido Agregar columnas.</span><span class="sxs-lookup"><span data-stu-id="e0d14-168">The application of a merge module can however change the schema of an existing database table if the module adds new columns to a table for which it is valid to add columns.</span></span> <span data-ttu-id="e0d14-169">Cuando se usa una versión de Mergemod.dll anterior a la versión 2,0, la aplicación de un módulo de combinación nunca cambia la longitud de las columnas y nunca cambia el esquema de la base de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="e0d14-169">When using a Mergemod.dll version less than version 2.0, the application of a merge module never changes the length of columns and never changes the schema of the target database.</span></span>

 

 



