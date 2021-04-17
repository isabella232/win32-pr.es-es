---
description: En la tabla ODBCDataSource se muestran los orígenes de datos que pertenecen a la instalación de.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: Tabla ODBCDataSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677462"
---
# <a name="odbcdatasource-table"></a><span data-ttu-id="723c7-103">Tabla ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="723c7-103">ODBCDataSource Table</span></span>

<span data-ttu-id="723c7-104">En la tabla ODBCDataSource se muestran los orígenes de datos que pertenecen a la instalación de.</span><span class="sxs-lookup"><span data-stu-id="723c7-104">The ODBCDataSource table lists the data sources belonging to the installation.</span></span>

<span data-ttu-id="723c7-105">La tabla ODBCDataSource tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="723c7-105">The ODBCDataSource table has the following columns.</span></span>



| <span data-ttu-id="723c7-106">Columna</span><span class="sxs-lookup"><span data-stu-id="723c7-106">Column</span></span>            | <span data-ttu-id="723c7-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="723c7-107">Type</span></span>                         | <span data-ttu-id="723c7-108">Clave</span><span class="sxs-lookup"><span data-stu-id="723c7-108">Key</span></span> | <span data-ttu-id="723c7-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="723c7-109">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="723c7-110">DataSource</span><span class="sxs-lookup"><span data-stu-id="723c7-110">DataSource</span></span>        | [<span data-ttu-id="723c7-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="723c7-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="723c7-112">Y</span><span class="sxs-lookup"><span data-stu-id="723c7-112">Y</span></span>   | <span data-ttu-id="723c7-113">N</span><span class="sxs-lookup"><span data-stu-id="723c7-113">N</span></span>        |
| <span data-ttu-id="723c7-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="723c7-114">Component\_</span></span>       | [<span data-ttu-id="723c7-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="723c7-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="723c7-116">N</span><span class="sxs-lookup"><span data-stu-id="723c7-116">N</span></span>   | <span data-ttu-id="723c7-117">N</span><span class="sxs-lookup"><span data-stu-id="723c7-117">N</span></span>        |
| <span data-ttu-id="723c7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="723c7-118">Description</span></span>       | [<span data-ttu-id="723c7-119">Texto</span><span class="sxs-lookup"><span data-stu-id="723c7-119">Text</span></span>](text.md)             | <span data-ttu-id="723c7-120">N</span><span class="sxs-lookup"><span data-stu-id="723c7-120">N</span></span>   | <span data-ttu-id="723c7-121">N</span><span class="sxs-lookup"><span data-stu-id="723c7-121">N</span></span>        |
| <span data-ttu-id="723c7-122">DriverDescription</span><span class="sxs-lookup"><span data-stu-id="723c7-122">DriverDescription</span></span> | [<span data-ttu-id="723c7-123">Texto</span><span class="sxs-lookup"><span data-stu-id="723c7-123">Text</span></span>](text.md)             | <span data-ttu-id="723c7-124">N</span><span class="sxs-lookup"><span data-stu-id="723c7-124">N</span></span>   | <span data-ttu-id="723c7-125">N</span><span class="sxs-lookup"><span data-stu-id="723c7-125">N</span></span>        |
| <span data-ttu-id="723c7-126">Registro</span><span class="sxs-lookup"><span data-stu-id="723c7-126">Registration</span></span>      | [<span data-ttu-id="723c7-127">Entero</span><span class="sxs-lookup"><span data-stu-id="723c7-127">Integer</span></span>](integer.md)       | <span data-ttu-id="723c7-128">N</span><span class="sxs-lookup"><span data-stu-id="723c7-128">N</span></span>   | <span data-ttu-id="723c7-129">N</span><span class="sxs-lookup"><span data-stu-id="723c7-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="723c7-130">Columnas</span><span class="sxs-lookup"><span data-stu-id="723c7-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="723c7-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource</span><span class="sxs-lookup"><span data-stu-id="723c7-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource</span></span>
</dt> <dd>

<span data-ttu-id="723c7-132">Nombre del token interno para el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="723c7-132">Internal token name for data source.</span></span> <span data-ttu-id="723c7-133">Clave principal de la tabla.</span><span class="sxs-lookup"><span data-stu-id="723c7-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="723c7-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="723c7-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="723c7-135">Clave externa en la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="723c7-135">External key into the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="723c7-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="723c7-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="723c7-137">Descripción registrada para este origen de datos.</span><span class="sxs-lookup"><span data-stu-id="723c7-137">The description registered for this data source.</span></span> <span data-ttu-id="723c7-138">Este valor no se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="723c7-138">This value cannot be localized.</span></span> <span data-ttu-id="723c7-139">Las descripciones de orígenes de datos ODBC no pueden superar la longitud de DSN de SQL \_ Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="723c7-139">ODBC data source descriptions cannot exceed SQL\_MAX\_DSN\_LENGTH.</span></span>

</dd> <dt>

<span data-ttu-id="723c7-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription</span><span class="sxs-lookup"><span data-stu-id="723c7-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription</span></span>
</dt> <dd>

<span data-ttu-id="723c7-141">Controlador asociado que puede estar ya existente.</span><span class="sxs-lookup"><span data-stu-id="723c7-141">Associated driver which may be pre-existing.</span></span> <span data-ttu-id="723c7-142">Este valor no se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="723c7-142">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="723c7-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Registro</span><span class="sxs-lookup"><span data-stu-id="723c7-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Registration</span></span>
</dt> <dd>

<span data-ttu-id="723c7-144">Este campo especifica el tipo de registro para el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="723c7-144">This field specifies the type of registration for the data source.</span></span>



| <span data-ttu-id="723c7-145">Constante</span><span class="sxs-lookup"><span data-stu-id="723c7-145">Constant</span></span>                                      | <span data-ttu-id="723c7-146">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="723c7-146">Hexadecimal</span></span> | <span data-ttu-id="723c7-147">Decimal</span><span class="sxs-lookup"><span data-stu-id="723c7-147">Decimal</span></span> | <span data-ttu-id="723c7-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="723c7-148">Description</span></span>                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| <span data-ttu-id="723c7-149">**msidbODBCDataSourceRegistrationPerMachine**</span><span class="sxs-lookup"><span data-stu-id="723c7-149">**msidbODBCDataSourceRegistrationPerMachine**</span></span> | <span data-ttu-id="723c7-150">0x000</span><span class="sxs-lookup"><span data-stu-id="723c7-150">0x000</span></span>       | <span data-ttu-id="723c7-151">0</span><span class="sxs-lookup"><span data-stu-id="723c7-151">0</span></span>       | <span data-ttu-id="723c7-152">El origen de datos se registra por equipo.</span><span class="sxs-lookup"><span data-stu-id="723c7-152">Data source is registered per machine.</span></span> |
| <span data-ttu-id="723c7-153">**msidbODBCDataSourceRegistrationPerUser**</span><span class="sxs-lookup"><span data-stu-id="723c7-153">**msidbODBCDataSourceRegistrationPerUser**</span></span>    | <span data-ttu-id="723c7-154">0x001</span><span class="sxs-lookup"><span data-stu-id="723c7-154">0x001</span></span>       | <span data-ttu-id="723c7-155">1</span><span class="sxs-lookup"><span data-stu-id="723c7-155">1</span></span>       | <span data-ttu-id="723c7-156">El origen de datos se registra por usuario.</span><span class="sxs-lookup"><span data-stu-id="723c7-156">Data source is registered per user.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="723c7-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="723c7-157">Remarks</span></span>

<span data-ttu-id="723c7-158">Las acciones [InstallODBC](installodbc-action.md) y [RemoveODBC](removeodbc-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="723c7-158">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="723c7-159">Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="723c7-159">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="723c7-160">Validación</span><span class="sxs-lookup"><span data-stu-id="723c7-160">Validation</span></span>

<dl>

[<span data-ttu-id="723c7-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="723c7-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="723c7-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="723c7-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="723c7-163">ICE32</span><span class="sxs-lookup"><span data-stu-id="723c7-163">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="723c7-164">ICE45</span><span class="sxs-lookup"><span data-stu-id="723c7-164">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="723c7-165">ICE98</span><span class="sxs-lookup"><span data-stu-id="723c7-165">ICE98</span></span>](ice98.md)  
</dl>

 

 



