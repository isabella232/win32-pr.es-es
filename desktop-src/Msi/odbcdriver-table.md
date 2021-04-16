---
description: En la tabla ODBCDriver se muestran los controladores ODBC que pertenecen a la instalación de.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Tabla ODBCDriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257f3eec5b60191df727d156572293489aa1956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541067"
---
# <a name="odbcdriver-table"></a><span data-ttu-id="39370-103">Tabla ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="39370-103">ODBCDriver Table</span></span>

<span data-ttu-id="39370-104">En la tabla ODBCDriver se muestran los controladores ODBC que pertenecen a la instalación de.</span><span class="sxs-lookup"><span data-stu-id="39370-104">The ODBCDriver table lists the ODBC drivers belonging to the installation.</span></span>

<span data-ttu-id="39370-105">La tabla ODBCDriver tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="39370-105">The ODBCDriver table has the following columns.</span></span>



| <span data-ttu-id="39370-106">Columna</span><span class="sxs-lookup"><span data-stu-id="39370-106">Column</span></span>      | <span data-ttu-id="39370-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="39370-107">Type</span></span>                         | <span data-ttu-id="39370-108">Clave</span><span class="sxs-lookup"><span data-stu-id="39370-108">Key</span></span> | <span data-ttu-id="39370-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="39370-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="39370-110">Controlador</span><span class="sxs-lookup"><span data-stu-id="39370-110">Driver</span></span>      | [<span data-ttu-id="39370-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="39370-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="39370-112">Y</span><span class="sxs-lookup"><span data-stu-id="39370-112">Y</span></span>   | <span data-ttu-id="39370-113">N</span><span class="sxs-lookup"><span data-stu-id="39370-113">N</span></span>        |
| <span data-ttu-id="39370-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="39370-114">Component\_</span></span> | [<span data-ttu-id="39370-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="39370-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="39370-116">N</span><span class="sxs-lookup"><span data-stu-id="39370-116">N</span></span>   | <span data-ttu-id="39370-117">N</span><span class="sxs-lookup"><span data-stu-id="39370-117">N</span></span>        |
| <span data-ttu-id="39370-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="39370-118">Description</span></span> | [<span data-ttu-id="39370-119">Texto</span><span class="sxs-lookup"><span data-stu-id="39370-119">Text</span></span>](text.md)             | <span data-ttu-id="39370-120">N</span><span class="sxs-lookup"><span data-stu-id="39370-120">N</span></span>   | <span data-ttu-id="39370-121">N</span><span class="sxs-lookup"><span data-stu-id="39370-121">N</span></span>        |
| <span data-ttu-id="39370-122">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="39370-122">File\_</span></span>      | [<span data-ttu-id="39370-123">Identificador</span><span class="sxs-lookup"><span data-stu-id="39370-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="39370-124">N</span><span class="sxs-lookup"><span data-stu-id="39370-124">N</span></span>   | <span data-ttu-id="39370-125">N</span><span class="sxs-lookup"><span data-stu-id="39370-125">N</span></span>        |
| <span data-ttu-id="39370-126">Configuración de archivos \_</span><span class="sxs-lookup"><span data-stu-id="39370-126">File\_Setup</span></span> | [<span data-ttu-id="39370-127">Identificador</span><span class="sxs-lookup"><span data-stu-id="39370-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="39370-128">N</span><span class="sxs-lookup"><span data-stu-id="39370-128">N</span></span>   | <span data-ttu-id="39370-129">Y</span><span class="sxs-lookup"><span data-stu-id="39370-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="39370-130">Columnas</span><span class="sxs-lookup"><span data-stu-id="39370-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="39370-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Dispositivo</span><span class="sxs-lookup"><span data-stu-id="39370-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Driver</span></span>
</dt> <dd>

<span data-ttu-id="39370-132">Nombre del token interno del controlador.</span><span class="sxs-lookup"><span data-stu-id="39370-132">Internal token name for driver.</span></span> <span data-ttu-id="39370-133">Una clave principal para la tabla</span><span class="sxs-lookup"><span data-stu-id="39370-133">A primary key for the table</span></span>

</dd> <dt>

<span data-ttu-id="39370-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="39370-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="39370-135">Clave externa en la tabla de componentes.</span><span class="sxs-lookup"><span data-stu-id="39370-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="39370-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="39370-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="39370-137">La descripción registrada para este controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="39370-137">The description registered for this ODBC driver.</span></span> <span data-ttu-id="39370-138">Este valor no se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="39370-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="39370-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_</span><span class="sxs-lookup"><span data-stu-id="39370-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="39370-140">El archivo DLL para los controladores enumerados en la columna controlador.</span><span class="sxs-lookup"><span data-stu-id="39370-140">The DLL file for drivers listed in the Driver column.</span></span> <span data-ttu-id="39370-141">La columna de archivo \_ es una clave externa de la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="39370-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="39370-142">El nombre de archivo especificado en la columna FILENAME de ese registro de tabla de archivos debe estar en el formato de nombre de archivo corto.</span><span class="sxs-lookup"><span data-stu-id="39370-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="39370-143">No se \| puede usar la sintaxis de LFN de SFN.</span><span class="sxs-lookup"><span data-stu-id="39370-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="39370-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuración de archivos \_</span><span class="sxs-lookup"><span data-stu-id="39370-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="39370-145">El archivo DLL de instalación del controlador si es diferente del controlador.</span><span class="sxs-lookup"><span data-stu-id="39370-145">The setup DLL file for the driver if it is different than from Driver.</span></span> <span data-ttu-id="39370-146">La columna de archivo \_ es una clave externa de la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="39370-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="39370-147">El nombre de archivo especificado en la columna FILENAME de ese registro de tabla de archivos debe estar en el formato de nombre de archivo corto.</span><span class="sxs-lookup"><span data-stu-id="39370-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="39370-148">No se \| puede usar la sintaxis de LFN de SFN.</span><span class="sxs-lookup"><span data-stu-id="39370-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39370-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39370-149">Remarks</span></span>

<span data-ttu-id="39370-150">Las acciones [InstallODBC](installodbc-action.md) y [RemoveODBC](removeodbc-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="39370-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="39370-151">Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="39370-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="39370-152">Validación</span><span class="sxs-lookup"><span data-stu-id="39370-152">Validation</span></span>

<dl>

[<span data-ttu-id="39370-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="39370-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="39370-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="39370-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="39370-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="39370-155">ICE32</span></span>](ice32.md)  
</dl>

 

 



