---
description: La \_ tabla de validación es una tabla del sistema que contiene los nombres de columna y los valores de columna de todas las tablas de la base de datos.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: _Validation tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666f00ccccda11706dce6a8d7e04e0efea91b7cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909161"
---
# <a name="_validation-table"></a><span data-ttu-id="11635-103">\_Tabla de validación</span><span class="sxs-lookup"><span data-stu-id="11635-103">\_Validation Table</span></span>

<span data-ttu-id="11635-104">La \_ tabla de validación es una tabla del sistema que contiene los nombres de columna y los valores de columna de todas las tablas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="11635-104">The \_Validation table is a system table that contains the column names and the column values for all of the tables in the database.</span></span> <span data-ttu-id="11635-105">Se utiliza durante el proceso de validación de la base de datos para asegurarse de que todas las columnas se han contabilizado y tienen los valores correctos.</span><span class="sxs-lookup"><span data-stu-id="11635-105">It is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="11635-106">Esta tabla no se incluye con la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="11635-106">This table is not shipped with the installer database.</span></span>

<span data-ttu-id="11635-107">La \_ tabla de validación tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="11635-107">The \_Validation table has the following columns.</span></span>



| <span data-ttu-id="11635-108">Columna</span><span class="sxs-lookup"><span data-stu-id="11635-108">Column</span></span>      | <span data-ttu-id="11635-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="11635-109">Type</span></span>                               | <span data-ttu-id="11635-110">Clave</span><span class="sxs-lookup"><span data-stu-id="11635-110">Key</span></span> | <span data-ttu-id="11635-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="11635-111">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="11635-112">Tabla</span><span class="sxs-lookup"><span data-stu-id="11635-112">Table</span></span>       | [<span data-ttu-id="11635-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="11635-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="11635-114">Y</span><span class="sxs-lookup"><span data-stu-id="11635-114">Y</span></span>   | <span data-ttu-id="11635-115">N</span><span class="sxs-lookup"><span data-stu-id="11635-115">N</span></span>        |
| <span data-ttu-id="11635-116">Columna</span><span class="sxs-lookup"><span data-stu-id="11635-116">Column</span></span>      | [<span data-ttu-id="11635-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="11635-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="11635-118">Y</span><span class="sxs-lookup"><span data-stu-id="11635-118">Y</span></span>   | <span data-ttu-id="11635-119">N</span><span class="sxs-lookup"><span data-stu-id="11635-119">N</span></span>        |
| <span data-ttu-id="11635-120">Nullable</span><span class="sxs-lookup"><span data-stu-id="11635-120">Nullable</span></span>    | [<span data-ttu-id="11635-121">Texto</span><span class="sxs-lookup"><span data-stu-id="11635-121">Text</span></span>](text.md)                   | <span data-ttu-id="11635-122">N</span><span class="sxs-lookup"><span data-stu-id="11635-122">N</span></span>   | <span data-ttu-id="11635-123">N</span><span class="sxs-lookup"><span data-stu-id="11635-123">N</span></span>        |
| <span data-ttu-id="11635-124">MinValue</span><span class="sxs-lookup"><span data-stu-id="11635-124">MinValue</span></span>    | [<span data-ttu-id="11635-125">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="11635-125">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="11635-126">N</span><span class="sxs-lookup"><span data-stu-id="11635-126">N</span></span>   | <span data-ttu-id="11635-127">Y</span><span class="sxs-lookup"><span data-stu-id="11635-127">Y</span></span>        |
| <span data-ttu-id="11635-128">MaxValue</span><span class="sxs-lookup"><span data-stu-id="11635-128">MaxValue</span></span>    | [<span data-ttu-id="11635-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="11635-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="11635-130">N</span><span class="sxs-lookup"><span data-stu-id="11635-130">N</span></span>   | <span data-ttu-id="11635-131">Y</span><span class="sxs-lookup"><span data-stu-id="11635-131">Y</span></span>        |
| <span data-ttu-id="11635-132">KeyTable</span><span class="sxs-lookup"><span data-stu-id="11635-132">KeyTable</span></span>    | [<span data-ttu-id="11635-133">Identificador</span><span class="sxs-lookup"><span data-stu-id="11635-133">Identifier</span></span>](identifier.md)       | <span data-ttu-id="11635-134">N</span><span class="sxs-lookup"><span data-stu-id="11635-134">N</span></span>   | <span data-ttu-id="11635-135">Y</span><span class="sxs-lookup"><span data-stu-id="11635-135">Y</span></span>        |
| <span data-ttu-id="11635-136">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="11635-136">KeyColumn</span></span>   | [<span data-ttu-id="11635-137">Entero</span><span class="sxs-lookup"><span data-stu-id="11635-137">Integer</span></span>](integer.md)             | <span data-ttu-id="11635-138">N</span><span class="sxs-lookup"><span data-stu-id="11635-138">N</span></span>   | <span data-ttu-id="11635-139">Y</span><span class="sxs-lookup"><span data-stu-id="11635-139">Y</span></span>        |
| <span data-ttu-id="11635-140">Category</span><span class="sxs-lookup"><span data-stu-id="11635-140">Category</span></span>    | [<span data-ttu-id="11635-141">Texto</span><span class="sxs-lookup"><span data-stu-id="11635-141">Text</span></span>](text.md)                   | <span data-ttu-id="11635-142">N</span><span class="sxs-lookup"><span data-stu-id="11635-142">N</span></span>   | <span data-ttu-id="11635-143">Y</span><span class="sxs-lookup"><span data-stu-id="11635-143">Y</span></span>        |
| <span data-ttu-id="11635-144">Set</span><span class="sxs-lookup"><span data-stu-id="11635-144">Set</span></span>         | [<span data-ttu-id="11635-145">Texto</span><span class="sxs-lookup"><span data-stu-id="11635-145">Text</span></span>](text.md)                   | <span data-ttu-id="11635-146">N</span><span class="sxs-lookup"><span data-stu-id="11635-146">N</span></span>   | <span data-ttu-id="11635-147">Y</span><span class="sxs-lookup"><span data-stu-id="11635-147">Y</span></span>        |
| <span data-ttu-id="11635-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="11635-148">Description</span></span> | [<span data-ttu-id="11635-149">Texto</span><span class="sxs-lookup"><span data-stu-id="11635-149">Text</span></span>](text.md)                   | <span data-ttu-id="11635-150">N</span><span class="sxs-lookup"><span data-stu-id="11635-150">N</span></span>   | <span data-ttu-id="11635-151">Y</span><span class="sxs-lookup"><span data-stu-id="11635-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="11635-152">Columnas</span><span class="sxs-lookup"><span data-stu-id="11635-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="11635-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro</span><span class="sxs-lookup"><span data-stu-id="11635-153"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="11635-154">Se utiliza para identificar una tabla determinada.</span><span class="sxs-lookup"><span data-stu-id="11635-154">Used to identify a particular table.</span></span> <span data-ttu-id="11635-155">Esta clave y la clave de columna forman la clave principal de la \_ tabla de validación.</span><span class="sxs-lookup"><span data-stu-id="11635-155">This key and the Column key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="11635-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Artículo</span><span class="sxs-lookup"><span data-stu-id="11635-156"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="11635-157">Se utiliza para identificar una columna determinada de la tabla.</span><span class="sxs-lookup"><span data-stu-id="11635-157">Used to identify a particular column of the table.</span></span> <span data-ttu-id="11635-158">Esta clave y la clave de tabla forman la clave principal de la \_ tabla de validación.</span><span class="sxs-lookup"><span data-stu-id="11635-158">This key and the Table key form the primary key of the \_Validation table.</span></span>

</dd> <dt>

<span data-ttu-id="11635-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Acepta valores NULL</span><span class="sxs-lookup"><span data-stu-id="11635-159"><span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable</span></span>
</dt> <dd>

<span data-ttu-id="11635-160">Identifica si la columna puede contener un valor null.</span><span class="sxs-lookup"><span data-stu-id="11635-160">Identifies whether the column may contain a Null value.</span></span>

<span data-ttu-id="11635-161">Esta columna puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="11635-161">This column may have one of the following values.</span></span>



| <span data-ttu-id="11635-162">String</span><span class="sxs-lookup"><span data-stu-id="11635-162">String</span></span> | <span data-ttu-id="11635-163">Significado</span><span class="sxs-lookup"><span data-stu-id="11635-163">Meaning</span></span>                                   |
|--------|-------------------------------------------|
| <span data-ttu-id="11635-164">Y</span><span class="sxs-lookup"><span data-stu-id="11635-164">Y</span></span>      | <span data-ttu-id="11635-165">Sí, la columna puede tener un valor null.</span><span class="sxs-lookup"><span data-stu-id="11635-165">Yes, the column may have a Null value.</span></span>    |
| <span data-ttu-id="11635-166">N</span><span class="sxs-lookup"><span data-stu-id="11635-166">N</span></span>      | <span data-ttu-id="11635-167">No, la columna no puede tener un valor null.</span><span class="sxs-lookup"><span data-stu-id="11635-167">No, the column may not have a Null value.</span></span> |



 

</dd> <dt>

<span data-ttu-id="11635-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span><span class="sxs-lookup"><span data-stu-id="11635-168"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue</span></span>
</dt> <dd>

<span data-ttu-id="11635-169">Este campo se aplica a las columnas que tienen un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="11635-169">This field applies to columns having numeric value.</span></span> <span data-ttu-id="11635-170">El campo contiene el valor mínimo permitido.</span><span class="sxs-lookup"><span data-stu-id="11635-170">The field contains the minimum permissible value.</span></span> <span data-ttu-id="11635-171">Puede ser el valor mínimo de un entero o el valor mínimo de una fecha o una cadena de versión.</span><span class="sxs-lookup"><span data-stu-id="11635-171">This can be the minimum value for an integer or the minimum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="11635-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span><span class="sxs-lookup"><span data-stu-id="11635-172"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue</span></span>
</dt> <dd>

<span data-ttu-id="11635-173">Este campo se aplica a las columnas que tienen un valor numérico.</span><span class="sxs-lookup"><span data-stu-id="11635-173">This field applies to columns having numeric value.</span></span> <span data-ttu-id="11635-174">El campo es el valor máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="11635-174">The field is the maximum permissible value.</span></span> <span data-ttu-id="11635-175">Puede ser el valor máximo de un entero o el valor máximo de una fecha o una cadena de versión.</span><span class="sxs-lookup"><span data-stu-id="11635-175">This may be the maximum value for an integer or the maximum value for a date or version string.</span></span>

</dd> <dt>

<span data-ttu-id="11635-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable</span><span class="sxs-lookup"><span data-stu-id="11635-176"><span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable</span></span>
</dt> <dd>

<span data-ttu-id="11635-177">Este campo se aplica a las columnas que son claves externas.</span><span class="sxs-lookup"><span data-stu-id="11635-177">This field applies to columns that are external keys.</span></span> <span data-ttu-id="11635-178">El campo identificado en la columna debe vincularse al número de columna especificado por KeyColumn en la tabla denominada en KeyTable.</span><span class="sxs-lookup"><span data-stu-id="11635-178">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="11635-179">Puede ser una lista de tablas separadas por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="11635-179">This can be a list of tables separated by semicolons.</span></span>

</dd> <dt>

<span data-ttu-id="11635-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span><span class="sxs-lookup"><span data-stu-id="11635-180"><span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn</span></span>
</dt> <dd>

<span data-ttu-id="11635-181">Este campo se aplica a las columnas de la tabla que son claves externas.</span><span class="sxs-lookup"><span data-stu-id="11635-181">This field applies to table columns that are external keys.</span></span> <span data-ttu-id="11635-182">El campo identificado en la columna debe vincularse al número de columna especificado por KeyColumn en la tabla denominada en KeyTable.</span><span class="sxs-lookup"><span data-stu-id="11635-182">The field identified in Column must link to the column number specified by KeyColumn in the table named in KeyTable.</span></span> <span data-ttu-id="11635-183">El intervalo permitido del campo KeyColumn es 1-32.</span><span class="sxs-lookup"><span data-stu-id="11635-183">The permissible range of the KeyColumn field is 1-32.</span></span>

</dd> <dt>

<span data-ttu-id="11635-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría</span><span class="sxs-lookup"><span data-stu-id="11635-184"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="11635-185">Es el tipo de datos que contiene el campo de base de datos especificado por las columnas de tabla y columna de la \_ tabla de validación.</span><span class="sxs-lookup"><span data-stu-id="11635-185">This is the type of data contained by the database field specified by the Table and Column columns of the \_Validation table.</span></span> <span data-ttu-id="11635-186">Si se trata de un tipo que tiene un valor numérico, como [Integer](integer.md), [DoubleInteger](doubleinteger.md) o [Time/Date](time-date.md), escriba null en este campo y especifique el intervalo del valor mediante las columnas MinValue y MaxValue.</span><span class="sxs-lookup"><span data-stu-id="11635-186">If this is a type having a numeric value, such as [Integer](integer.md), [DoubleInteger](doubleinteger.md) or [Time/Date](time-date.md), then enter null into this field and specify the value's range using the MinValue and MaxValue columns.</span></span> <span data-ttu-id="11635-187">Utilice la columna categoría para especificar los tipos de datos no numéricos que se describen en [tipos de datos de columna](column-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="11635-187">Use the Category column to specify the non-numeric data types described in [Column Data Types](column-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="11635-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Conjunto</span><span class="sxs-lookup"><span data-stu-id="11635-188"><span id="Set"></span><span id="set"></span><span id="SET"></span>Set</span></span>
</dt> <dd>

<span data-ttu-id="11635-189">Esta es una lista de valores permitidos para este campo separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="11635-189">This is a list of permissible values for this field separated by semicolons.</span></span> <span data-ttu-id="11635-190">Este campo se utiliza normalmente para las enumeraciones.</span><span class="sxs-lookup"><span data-stu-id="11635-190">This field is usually used for enumerations.</span></span>

</dd> <dt>

<span data-ttu-id="11635-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="11635-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="11635-192">Descripción de los datos que se almacenan en la columna.</span><span class="sxs-lookup"><span data-stu-id="11635-192">A description of the data that is stored in the column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="11635-193">Validación</span><span class="sxs-lookup"><span data-stu-id="11635-193">Validation</span></span>

<dl>

[<span data-ttu-id="11635-194">ICE03</span><span class="sxs-lookup"><span data-stu-id="11635-194">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="11635-195">ICE06</span><span class="sxs-lookup"><span data-stu-id="11635-195">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="11635-196">ICE32</span><span class="sxs-lookup"><span data-stu-id="11635-196">ICE32</span></span>](ice32.md)  
</dl>

## <a name="remarks"></a><span data-ttu-id="11635-197">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11635-197">Remarks</span></span>

<span data-ttu-id="11635-198">El campo Category de esta tabla solo se aplica a los datos de cadena.</span><span class="sxs-lookup"><span data-stu-id="11635-198">The Category field of this table only applies to string data.</span></span> <span data-ttu-id="11635-199">Si el campo de columna hace referencia a una columna con datos binarios, el tipo de datos binarios debe especificarse en el campo categoría.</span><span class="sxs-lookup"><span data-stu-id="11635-199">If the Column field refers to a column with binary data, the binary data type must be specified in the Category field.</span></span> <span data-ttu-id="11635-200">Los tipos de columna de datos enteros omiten el campo de categoría durante la validación.</span><span class="sxs-lookup"><span data-stu-id="11635-200">Integer data Column types ignore the Category field during validation.</span></span>

 

 



