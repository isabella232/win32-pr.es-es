---
description: Se trata de una tabla temporal de solo lectura que se usa para ver las transformaciones con el modo de vista de transformación. El instalador nunca conserva esta tabla.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: _TransformView tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545203"
---
# <a name="_transformview-table"></a><span data-ttu-id="5181d-104">\_Tabla TransformView</span><span class="sxs-lookup"><span data-stu-id="5181d-104">\_TransformView Table</span></span>

<span data-ttu-id="5181d-105">Se trata de una tabla temporal de solo lectura que se usa para ver las transformaciones con el modo de vista de transformación.</span><span class="sxs-lookup"><span data-stu-id="5181d-105">This is a read-only temporary table used to view transforms with the transform view mode.</span></span> <span data-ttu-id="5181d-106">El instalador nunca conserva esta tabla.</span><span class="sxs-lookup"><span data-stu-id="5181d-106">This table is never persisted by the installer.</span></span>

<span data-ttu-id="5181d-107">Para invocar el modo de vista de transformación, obtenga un identificador y abra la base de datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="5181d-107">To invoke the transform view mode, obtain a handle and open the reference database.</span></span> <span data-ttu-id="5181d-108">Vea [obtener un identificador de base de datos](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="5181d-108">See [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span> <span data-ttu-id="5181d-109">Llame a [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) con MSITRANSFORM \_ error \_ VIEWTRANSFORM.</span><span class="sxs-lookup"><span data-stu-id="5181d-109">Call [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) with MSITRANSFORM\_ERROR\_VIEWTRANSFORM.</span></span> <span data-ttu-id="5181d-110">Esto impide que la transformación se aplique a la base de datos y vuelca el contenido de la transformación en la \_ tabla TransformView.</span><span class="sxs-lookup"><span data-stu-id="5181d-110">This stops the transform from being applied to the database and dumps the transform contents into the \_TransformView table.</span></span> <span data-ttu-id="5181d-111">Se puede tener acceso a los datos de la tabla mediante consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="5181d-111">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="5181d-112">Vea [trabajar con consultas](working-with-queries.md).</span><span class="sxs-lookup"><span data-stu-id="5181d-112">See [Working with Queries](working-with-queries.md).</span></span>

<span data-ttu-id="5181d-113">La \_ tabla TransformView no se borra cuando se aplica otra transformación.</span><span class="sxs-lookup"><span data-stu-id="5181d-113">The \_TransformView table is not cleared when another transform is applied.</span></span> <span data-ttu-id="5181d-114">La tabla refleja el efecto acumulativo de las aplicaciones sucesivas.</span><span class="sxs-lookup"><span data-stu-id="5181d-114">The table reflects the cumulative effect of successive applications.</span></span> <span data-ttu-id="5181d-115">Para ver las transformaciones por separado, debe liberar la tabla.</span><span class="sxs-lookup"><span data-stu-id="5181d-115">To view the transforms separately you must release the table.</span></span>

<span data-ttu-id="5181d-116">La \_ tabla TransformView tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="5181d-116">The \_TransformView Table has the following columns.</span></span>



| <span data-ttu-id="5181d-117">Columna</span><span class="sxs-lookup"><span data-stu-id="5181d-117">Column</span></span>  | <span data-ttu-id="5181d-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="5181d-118">Type</span></span>                         | <span data-ttu-id="5181d-119">Clave</span><span class="sxs-lookup"><span data-stu-id="5181d-119">Key</span></span> | <span data-ttu-id="5181d-120">Nullable</span><span class="sxs-lookup"><span data-stu-id="5181d-120">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="5181d-121">Tabla</span><span class="sxs-lookup"><span data-stu-id="5181d-121">Table</span></span>   | [<span data-ttu-id="5181d-122">Identificador</span><span class="sxs-lookup"><span data-stu-id="5181d-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="5181d-123">Y</span><span class="sxs-lookup"><span data-stu-id="5181d-123">Y</span></span>   | <span data-ttu-id="5181d-124">N</span><span class="sxs-lookup"><span data-stu-id="5181d-124">N</span></span>        |
| <span data-ttu-id="5181d-125">Columna</span><span class="sxs-lookup"><span data-stu-id="5181d-125">Column</span></span>  | [<span data-ttu-id="5181d-126">Texto</span><span class="sxs-lookup"><span data-stu-id="5181d-126">Text</span></span>](text.md)             | <span data-ttu-id="5181d-127">Y</span><span class="sxs-lookup"><span data-stu-id="5181d-127">Y</span></span>   | <span data-ttu-id="5181d-128">N</span><span class="sxs-lookup"><span data-stu-id="5181d-128">N</span></span>        |
| <span data-ttu-id="5181d-129">Row</span><span class="sxs-lookup"><span data-stu-id="5181d-129">Row</span></span>     | [<span data-ttu-id="5181d-130">Texto</span><span class="sxs-lookup"><span data-stu-id="5181d-130">Text</span></span>](text.md)             | <span data-ttu-id="5181d-131">Y</span><span class="sxs-lookup"><span data-stu-id="5181d-131">Y</span></span>   | <span data-ttu-id="5181d-132">Y</span><span class="sxs-lookup"><span data-stu-id="5181d-132">Y</span></span>        |
| <span data-ttu-id="5181d-133">Datos</span><span class="sxs-lookup"><span data-stu-id="5181d-133">Data</span></span>    | [<span data-ttu-id="5181d-134">Texto</span><span class="sxs-lookup"><span data-stu-id="5181d-134">Text</span></span>](text.md)             | <span data-ttu-id="5181d-135">N</span><span class="sxs-lookup"><span data-stu-id="5181d-135">N</span></span>   | <span data-ttu-id="5181d-136">Y</span><span class="sxs-lookup"><span data-stu-id="5181d-136">Y</span></span>        |
| <span data-ttu-id="5181d-137">Current</span><span class="sxs-lookup"><span data-stu-id="5181d-137">Current</span></span> | [<span data-ttu-id="5181d-138">Texto</span><span class="sxs-lookup"><span data-stu-id="5181d-138">Text</span></span>](text.md)             | <span data-ttu-id="5181d-139">N</span><span class="sxs-lookup"><span data-stu-id="5181d-139">N</span></span>   | <span data-ttu-id="5181d-140">Y</span><span class="sxs-lookup"><span data-stu-id="5181d-140">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="5181d-141">Columna</span><span class="sxs-lookup"><span data-stu-id="5181d-141">Column</span></span>

<dl> <dt>

<span data-ttu-id="5181d-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro</span><span class="sxs-lookup"><span data-stu-id="5181d-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="5181d-143">Nombre de una tabla de base de datos modificada.</span><span class="sxs-lookup"><span data-stu-id="5181d-143">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="5181d-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Artículo</span><span class="sxs-lookup"><span data-stu-id="5181d-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="5181d-145">Nombre de una columna de tabla alterada o inserción, eliminación, creación o eliminación.</span><span class="sxs-lookup"><span data-stu-id="5181d-145">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="5181d-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Columna</span><span class="sxs-lookup"><span data-stu-id="5181d-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="5181d-147">Una lista de los valores de clave principal separados por tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="5181d-147">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="5181d-148">Los valores de clave principal NULL se representan mediante un solo carácter de espacio.</span><span class="sxs-lookup"><span data-stu-id="5181d-148">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="5181d-149">Un valor null en esta columna indica un cambio de esquema.</span><span class="sxs-lookup"><span data-stu-id="5181d-149">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="5181d-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span><span class="sxs-lookup"><span data-stu-id="5181d-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="5181d-151">Los datos, el nombre de un flujo de datos o una definición de columna.</span><span class="sxs-lookup"><span data-stu-id="5181d-151">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="5181d-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Corrientes</span><span class="sxs-lookup"><span data-stu-id="5181d-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="5181d-153">Valor actual de la base de datos de referencia o de una columna a un número.</span><span class="sxs-lookup"><span data-stu-id="5181d-153">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5181d-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5181d-154">Remarks</span></span>

<span data-ttu-id="5181d-155">El \_ TransformView se mantiene en la memoria por un recuento de bloqueos, que se puede liberar con el siguiente comando SQL.</span><span class="sxs-lookup"><span data-stu-id="5181d-155">The \_TransformView is held in memory by a lock count, that can be released with the following SQL command.</span></span>

<span data-ttu-id="5181d-156">"ALTER TABLE \_ TRANSFORMVIEW Free".</span><span class="sxs-lookup"><span data-stu-id="5181d-156">"ALTER TABLE \_TransformView FREE".</span></span>

<span data-ttu-id="5181d-157">Se puede tener acceso a los datos de la tabla mediante consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="5181d-157">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="5181d-158">El lenguaje SQL tiene dos divisiones principales: lenguaje de definición de datos (DDL) que se usa para definir todos los objetos de una base de datos SQL, y el lenguaje de manipulación de datos (DML) que se utiliza para seleccionar, insertar, actualizar y eliminar datos en los objetos definidos mediante DDL.</span><span class="sxs-lookup"><span data-stu-id="5181d-158">The SQL language has two main divisions: Data Definition Language (DDL) that is used to define all the objects in an SQL database, and Data Manipulation Language (DML) that is used to select, insert, update, and delete data in the objects defined using DDL.</span></span>

<span data-ttu-id="5181d-159">Las operaciones de transformación del lenguaje de manipulación de datos (DML) se indican como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="5181d-159">The Data Manipulation Language (DML) transform operations are indicated as follows.</span></span> <span data-ttu-id="5181d-160">El lenguaje de manipulación de datos (DML) son las instrucciones de SQL que manipulan los datos, en lugar de definirlos.</span><span class="sxs-lookup"><span data-stu-id="5181d-160">Data Manipulation Language (DML) are those statements in SQL that manipulate, as opposed to define, data.</span></span>



| <span data-ttu-id="5181d-161">Operación de transformación</span><span class="sxs-lookup"><span data-stu-id="5181d-161">Transform operation</span></span> | <span data-ttu-id="5181d-162">Resultado de SQL</span><span class="sxs-lookup"><span data-stu-id="5181d-162">SQL result</span></span>                                    |
|---------------------|-----------------------------------------------|
| <span data-ttu-id="5181d-163">Modificar datos</span><span class="sxs-lookup"><span data-stu-id="5181d-163">Modify data</span></span>         | <span data-ttu-id="5181d-164">cuadro artículo columna Data {valor actual}</span><span class="sxs-lookup"><span data-stu-id="5181d-164">{table} {column} {row} {data} {current value}</span></span> |
| <span data-ttu-id="5181d-165">Insertar fila</span><span class="sxs-lookup"><span data-stu-id="5181d-165">Insert row</span></span>          | <span data-ttu-id="5181d-166">cuadro "INSERT" {Row} null null</span><span class="sxs-lookup"><span data-stu-id="5181d-166">{table} "INSERT" {row} NULL NULL</span></span>              |
| <span data-ttu-id="5181d-167">Eliminar fila</span><span class="sxs-lookup"><span data-stu-id="5181d-167">Delete row</span></span>          | <span data-ttu-id="5181d-168">cuadro "Eliminar" {Row} null null</span><span class="sxs-lookup"><span data-stu-id="5181d-168">{table} "DELETE" {row} NULL NULL</span></span>              |



 

<span data-ttu-id="5181d-169">Las operaciones de transformación del lenguaje de definición de datos (DDL) se indican como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="5181d-169">The Data Definition Language (DDL) transform operations are indicated as follows.</span></span> <span data-ttu-id="5181d-170">El lenguaje de definición de datos (DDL) son las instrucciones de SQL que definen, en lugar de manipular los datos.</span><span class="sxs-lookup"><span data-stu-id="5181d-170">Data Definition Language (DDL) are those statements in SQL that define, as opposed to manipulate, data.</span></span>



| <span data-ttu-id="5181d-171">Operación de transformación</span><span class="sxs-lookup"><span data-stu-id="5181d-171">Transform operation</span></span> | <span data-ttu-id="5181d-172">Resultado de SQL</span><span class="sxs-lookup"><span data-stu-id="5181d-172">SQL result</span></span>                                   |
|---------------------|----------------------------------------------|
| <span data-ttu-id="5181d-173">Agregar columna</span><span class="sxs-lookup"><span data-stu-id="5181d-173">Add column</span></span>          | <span data-ttu-id="5181d-174">cuadro artículo NULL {defn} {número de columna}</span><span class="sxs-lookup"><span data-stu-id="5181d-174">{table} {column} NULL {defn} {column number}</span></span> |
| <span data-ttu-id="5181d-175">Agregar tabla</span><span class="sxs-lookup"><span data-stu-id="5181d-175">Add table</span></span>           | <span data-ttu-id="5181d-176">cuadro "CREATE" NULL NULL NULL</span><span class="sxs-lookup"><span data-stu-id="5181d-176">{table} "CREATE" NULL NULL NULL</span></span>              |
| <span data-ttu-id="5181d-177">Quitar tabla</span><span class="sxs-lookup"><span data-stu-id="5181d-177">Drop table</span></span>          | <span data-ttu-id="5181d-178">cuadro "DROP" NULL NULL NULL</span><span class="sxs-lookup"><span data-stu-id="5181d-178">{table} "DROP" NULL NULL NULL</span></span>                |



 

<span data-ttu-id="5181d-179">Cuando la aplicación de una transformación agrega esta tabla, el campo de datos recibe texto que se puede interpretar como un valor entero de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5181d-179">When the application of a transform adds this table, the Data field receives text that can be interpreted as a 16-bit integer value.</span></span> <span data-ttu-id="5181d-180">El valor describe la columna mencionada en el campo de columna.</span><span class="sxs-lookup"><span data-stu-id="5181d-180">The value describes the column named in the Column field.</span></span> <span data-ttu-id="5181d-181">Puede comparar el valor entero con las constantes de la tabla siguiente para determinar la definición de la columna modificada.</span><span class="sxs-lookup"><span data-stu-id="5181d-181">You can compare the integer value to the constants in the following table to determine the definition of the altered column.</span></span>



| <span data-ttu-id="5181d-182">bit</span><span class="sxs-lookup"><span data-stu-id="5181d-182">Bit</span></span>                                                                                                       | <span data-ttu-id="5181d-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="5181d-183">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5181d-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7</span><span class="sxs-lookup"><span data-stu-id="5181d-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7</span></span><br/>         | <span data-ttu-id="5181d-185">Hexadecimal: 0x0000 0x0100</span><span class="sxs-lookup"><span data-stu-id="5181d-185">Hexadecimal: 0x0000 0x0100</span></span><br/> <span data-ttu-id="5181d-186">Decimal: 0 255</span><span class="sxs-lookup"><span data-stu-id="5181d-186">Decimal: 0 255</span></span><br/> <span data-ttu-id="5181d-187">Ancho de columna</span><span class="sxs-lookup"><span data-stu-id="5181d-187">Column width</span></span><br/>                                                                                                                                                                                                                                  |
| <span data-ttu-id="5181d-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8</span><span class="sxs-lookup"><span data-stu-id="5181d-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8</span></span><br/>                  | <span data-ttu-id="5181d-189">Hexadecimal: 0x0100</span><span class="sxs-lookup"><span data-stu-id="5181d-189">Hexadecimal: 0x0100</span></span><br/> <span data-ttu-id="5181d-190">Decimal: 256</span><span class="sxs-lookup"><span data-stu-id="5181d-190">Decimal: 256</span></span><br/> <span data-ttu-id="5181d-191">Una columna persistente.</span><span class="sxs-lookup"><span data-stu-id="5181d-191">A persistent column.</span></span> <span data-ttu-id="5181d-192">Cero significa una columna temporal.</span><span class="sxs-lookup"><span data-stu-id="5181d-192">Zero means a temporary column.</span></span> <br/>                                                                                                                                                                                                   |
| <span data-ttu-id="5181d-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9</span><span class="sxs-lookup"><span data-stu-id="5181d-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9</span></span><br/>                  | <span data-ttu-id="5181d-194">Hexadecimal: 0x0200</span><span class="sxs-lookup"><span data-stu-id="5181d-194">Hexadecimal: 0x0200</span></span><br/> <span data-ttu-id="5181d-195">Decimal: 1023</span><span class="sxs-lookup"><span data-stu-id="5181d-195">Decimal: 1023</span></span><br/> <span data-ttu-id="5181d-196">Una columna localizable.</span><span class="sxs-lookup"><span data-stu-id="5181d-196">A localizable column.</span></span> <span data-ttu-id="5181d-197">Cero significa que la columna no se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="5181d-197">Zero means the column cannot be localized.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="5181d-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span><span class="sxs-lookup"><span data-stu-id="5181d-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span></span><br/> | <span data-ttu-id="5181d-199">Hexadecimal: 0x0000</span><span class="sxs-lookup"><span data-stu-id="5181d-199">Hexadecimal: 0x0000</span></span><br/> <span data-ttu-id="5181d-200">Decimal: 0</span><span class="sxs-lookup"><span data-stu-id="5181d-200">Decimal: 0</span></span><br/> <span data-ttu-id="5181d-201">Entero largo</span><span class="sxs-lookup"><span data-stu-id="5181d-201">Long integer</span></span><br/> <span data-ttu-id="5181d-202">Hexadecimal: 0x0400</span><span class="sxs-lookup"><span data-stu-id="5181d-202">Hexadecimal: 0x0400</span></span><br/> <span data-ttu-id="5181d-203">Decimal: 1024</span><span class="sxs-lookup"><span data-stu-id="5181d-203">Decimal: 1024</span></span><br/> <span data-ttu-id="5181d-204">Entero corto</span><span class="sxs-lookup"><span data-stu-id="5181d-204">Short integer</span></span><br/> <span data-ttu-id="5181d-205">Hexadecimal: 0x0800</span><span class="sxs-lookup"><span data-stu-id="5181d-205">Hexadecimal: 0x0800</span></span><br/> <span data-ttu-id="5181d-206">Decimal: 2048</span><span class="sxs-lookup"><span data-stu-id="5181d-206">Decimal: 2048</span></span><br/> <span data-ttu-id="5181d-207">Objeto binario</span><span class="sxs-lookup"><span data-stu-id="5181d-207">Binary object</span></span><br/> <span data-ttu-id="5181d-208">Hexadecimal: 0x0C00</span><span class="sxs-lookup"><span data-stu-id="5181d-208">Hexadecimal: 0x0C00</span></span><br/> <span data-ttu-id="5181d-209">Decimal: 3072</span><span class="sxs-lookup"><span data-stu-id="5181d-209">Decimal: 3072</span></span><br/> <span data-ttu-id="5181d-210">String</span><span class="sxs-lookup"><span data-stu-id="5181d-210">String</span></span><br/> |
| <span data-ttu-id="5181d-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span><span class="sxs-lookup"><span data-stu-id="5181d-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span></span><br/>              | <span data-ttu-id="5181d-212">Hexadecimal: 0x1000</span><span class="sxs-lookup"><span data-stu-id="5181d-212">Hexadecimal: 0x1000</span></span><br/> <span data-ttu-id="5181d-213">Decimal: 4096</span><span class="sxs-lookup"><span data-stu-id="5181d-213">Decimal: 4096</span></span><br/> <span data-ttu-id="5181d-214">Columna que admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="5181d-214">Nullable column.</span></span> <span data-ttu-id="5181d-215">Cero significa que la columna no acepta valores NULL.</span><span class="sxs-lookup"><span data-stu-id="5181d-215">Zero means the column is non-nullable.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="5181d-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span><span class="sxs-lookup"><span data-stu-id="5181d-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span></span><br/>              | <span data-ttu-id="5181d-217">Hexadecimal: 0x2000</span><span class="sxs-lookup"><span data-stu-id="5181d-217">Hexadecimal: 0x2000</span></span><br/> <span data-ttu-id="5181d-218">Decimal: 8192</span><span class="sxs-lookup"><span data-stu-id="5181d-218">Decimal: 8192</span></span><br/> <span data-ttu-id="5181d-219">Columna de clave principal.</span><span class="sxs-lookup"><span data-stu-id="5181d-219">Primary key column.</span></span> <span data-ttu-id="5181d-220">Cero significa que esta columna no es una clave principal.</span><span class="sxs-lookup"><span data-stu-id="5181d-220">Zero means this column is not a primary key.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="5181d-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15</span><span class="sxs-lookup"><span data-stu-id="5181d-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15</span></span><br/> | <span data-ttu-id="5181d-222">Hexadecimal: 0x4000 0x8000</span><span class="sxs-lookup"><span data-stu-id="5181d-222">Hexadecimal: 0x4000 0x8000</span></span><br/> <span data-ttu-id="5181d-223">Decimal: 16384 32768</span><span class="sxs-lookup"><span data-stu-id="5181d-223">Decimal: 16384 32768</span></span><br/> <span data-ttu-id="5181d-224">Reservado</span><span class="sxs-lookup"><span data-stu-id="5181d-224">Reserved</span></span><br/>                                                                                                                                                                                                                                |



 

<span data-ttu-id="5181d-225">Para obtener un ejemplo de script que muestre la \_ tabla TransformView, vea [ver una transformación](view-a-transform.md).</span><span class="sxs-lookup"><span data-stu-id="5181d-225">For a script sample that demonstrates the \_TransformView table, see [View a Transform](view-a-transform.md).</span></span>

 

 




