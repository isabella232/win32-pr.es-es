---
description: La \_ tabla de columnas es una tabla del sistema de solo lectura que contiene el catálogo de columnas. Muestra las columnas de todas las tablas. Puede consultar esta tabla para averiguar si existe una columna determinada.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: _Columns tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667084"
---
# <a name="_columns-table"></a><span data-ttu-id="1add6-105">\_Tabla de columnas</span><span class="sxs-lookup"><span data-stu-id="1add6-105">\_Columns Table</span></span>

<span data-ttu-id="1add6-106">La \_ tabla de columnas es una tabla del sistema de solo lectura que contiene el catálogo de columnas.</span><span class="sxs-lookup"><span data-stu-id="1add6-106">The \_Columns table is a read-only system table that contains the column catalog.</span></span> <span data-ttu-id="1add6-107">Muestra las columnas de todas las tablas.</span><span class="sxs-lookup"><span data-stu-id="1add6-107">It lists the columns for all the tables.</span></span> <span data-ttu-id="1add6-108">Puede consultar esta tabla para averiguar si existe una columna determinada.</span><span class="sxs-lookup"><span data-stu-id="1add6-108">You can query this table to find out if a given column exists.</span></span>

<span data-ttu-id="1add6-109">La \_ tabla de columnas tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="1add6-109">The \_Columns table has the following columns.</span></span>



| <span data-ttu-id="1add6-110">Columna</span><span class="sxs-lookup"><span data-stu-id="1add6-110">Column</span></span> | <span data-ttu-id="1add6-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="1add6-111">Type</span></span>                   | <span data-ttu-id="1add6-112">Clave</span><span class="sxs-lookup"><span data-stu-id="1add6-112">Key</span></span> | <span data-ttu-id="1add6-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="1add6-113">Nullable</span></span> |
|--------|------------------------|-----|----------|
| <span data-ttu-id="1add6-114">Tabla</span><span class="sxs-lookup"><span data-stu-id="1add6-114">Table</span></span>  | [<span data-ttu-id="1add6-115">Texto</span><span class="sxs-lookup"><span data-stu-id="1add6-115">Text</span></span>](text.md)       | <span data-ttu-id="1add6-116">Y</span><span class="sxs-lookup"><span data-stu-id="1add6-116">Y</span></span>   | <span data-ttu-id="1add6-117">N</span><span class="sxs-lookup"><span data-stu-id="1add6-117">N</span></span>        |
| <span data-ttu-id="1add6-118">Number</span><span class="sxs-lookup"><span data-stu-id="1add6-118">Number</span></span> | [<span data-ttu-id="1add6-119">Entero</span><span class="sxs-lookup"><span data-stu-id="1add6-119">Integer</span></span>](integer.md) | <span data-ttu-id="1add6-120">Y</span><span class="sxs-lookup"><span data-stu-id="1add6-120">Y</span></span>   | <span data-ttu-id="1add6-121">N</span><span class="sxs-lookup"><span data-stu-id="1add6-121">N</span></span>        |
| <span data-ttu-id="1add6-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="1add6-122">Name</span></span>   | [<span data-ttu-id="1add6-123">Texto</span><span class="sxs-lookup"><span data-stu-id="1add6-123">Text</span></span>](text.md)       | <span data-ttu-id="1add6-124">N</span><span class="sxs-lookup"><span data-stu-id="1add6-124">N</span></span>   | <span data-ttu-id="1add6-125">N</span><span class="sxs-lookup"><span data-stu-id="1add6-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1add6-126">Columnas</span><span class="sxs-lookup"><span data-stu-id="1add6-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1add6-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro</span><span class="sxs-lookup"><span data-stu-id="1add6-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="1add6-128">El nombre de la tabla que contiene la columna.</span><span class="sxs-lookup"><span data-stu-id="1add6-128">The name of the table that contains the column.</span></span>

</dd> <dt>

<span data-ttu-id="1add6-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Números</span><span class="sxs-lookup"><span data-stu-id="1add6-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Number</span></span>
</dt> <dd>

<span data-ttu-id="1add6-130">El orden de la columna dentro de la tabla.</span><span class="sxs-lookup"><span data-stu-id="1add6-130">The order of the column within the table.</span></span>

</dd> <dt>

<span data-ttu-id="1add6-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="1add6-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="1add6-132">El nombre de la columna.</span><span class="sxs-lookup"><span data-stu-id="1add6-132">The name of the column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1add6-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1add6-133">Remarks</span></span>

<span data-ttu-id="1add6-134">Dado \_ que la tabla de columnas es una tabla del sistema que no se puede modificar mediante consultas SQL, no puede obtener las claves principales con la función [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) o la [**propiedad PrimaryKeys**](database-primarykeys.md).</span><span class="sxs-lookup"><span data-stu-id="1add6-134">Because the \_Columns table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

<span data-ttu-id="1add6-135">Solo las columnas persistentes se almacenan en la \_ tabla de columnas.</span><span class="sxs-lookup"><span data-stu-id="1add6-135">Only persistent columns are stored in the \_Columns table.</span></span> <span data-ttu-id="1add6-136">Para determinar si existe una columna temporal, es necesario crear una vista mediante una instrucción SELECT \* en la tabla y, a continuación, recorrer todos los campos de un registro devueltos por la función [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) con la \_ opción MSICOLINFO Names.</span><span class="sxs-lookup"><span data-stu-id="1add6-136">To determine if a temporary column exists one would need to create a view using a SELECT \* statement against the table, then loop through all fields in a record returned by the [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) function with the MSICOLINFO\_NAMES option.</span></span>

 

 



