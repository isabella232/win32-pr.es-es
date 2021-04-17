---
description: En la tabla ODBCTranslator se enumeran los traductores ODBC que pertenecen a la instalación de.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Tabla ODBCTranslator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653055"
---
# <a name="odbctranslator-table"></a><span data-ttu-id="6f3e1-103">Tabla ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="6f3e1-103">ODBCTranslator Table</span></span>

<span data-ttu-id="6f3e1-104">En la tabla ODBCTranslator se enumeran los traductores ODBC que pertenecen a la instalación de.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-104">The ODBCTranslator table lists the ODBC translators belonging to the installation.</span></span>

<span data-ttu-id="6f3e1-105">La tabla ODBCTranslator tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-105">The ODBCTranslator table has the following columns.</span></span>



| <span data-ttu-id="6f3e1-106">Columna</span><span class="sxs-lookup"><span data-stu-id="6f3e1-106">Column</span></span>      | <span data-ttu-id="6f3e1-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f3e1-107">Type</span></span>                         | <span data-ttu-id="6f3e1-108">Clave</span><span class="sxs-lookup"><span data-stu-id="6f3e1-108">Key</span></span> | <span data-ttu-id="6f3e1-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="6f3e1-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="6f3e1-110">Translator</span><span class="sxs-lookup"><span data-stu-id="6f3e1-110">Translator</span></span>  | [<span data-ttu-id="6f3e1-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="6f3e1-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="6f3e1-112">Y</span><span class="sxs-lookup"><span data-stu-id="6f3e1-112">Y</span></span>   | <span data-ttu-id="6f3e1-113">N</span><span class="sxs-lookup"><span data-stu-id="6f3e1-113">N</span></span>        |
| <span data-ttu-id="6f3e1-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="6f3e1-114">Component\_</span></span> | [<span data-ttu-id="6f3e1-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="6f3e1-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="6f3e1-116">N</span><span class="sxs-lookup"><span data-stu-id="6f3e1-116">N</span></span>   | <span data-ttu-id="6f3e1-117">N</span><span class="sxs-lookup"><span data-stu-id="6f3e1-117">N</span></span>        |
| <span data-ttu-id="6f3e1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f3e1-118">Description</span></span> | [<span data-ttu-id="6f3e1-119">Texto</span><span class="sxs-lookup"><span data-stu-id="6f3e1-119">Text</span></span>](text.md)             | <span data-ttu-id="6f3e1-120">N</span><span class="sxs-lookup"><span data-stu-id="6f3e1-120">N</span></span>   | <span data-ttu-id="6f3e1-121">N</span><span class="sxs-lookup"><span data-stu-id="6f3e1-121">N</span></span>        |
| <span data-ttu-id="6f3e1-122">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="6f3e1-122">File\_</span></span>      | [<span data-ttu-id="6f3e1-123">Identificador</span><span class="sxs-lookup"><span data-stu-id="6f3e1-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="6f3e1-124">N</span><span class="sxs-lookup"><span data-stu-id="6f3e1-124">N</span></span>   | <span data-ttu-id="6f3e1-125">N</span><span class="sxs-lookup"><span data-stu-id="6f3e1-125">N</span></span>        |
| <span data-ttu-id="6f3e1-126">Configuración de archivos \_</span><span class="sxs-lookup"><span data-stu-id="6f3e1-126">File\_Setup</span></span> | [<span data-ttu-id="6f3e1-127">Identificador</span><span class="sxs-lookup"><span data-stu-id="6f3e1-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="6f3e1-128">N</span><span class="sxs-lookup"><span data-stu-id="6f3e1-128">N</span></span>   | <span data-ttu-id="6f3e1-129">Y</span><span class="sxs-lookup"><span data-stu-id="6f3e1-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6f3e1-130">Columnas</span><span class="sxs-lookup"><span data-stu-id="6f3e1-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6f3e1-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span><span class="sxs-lookup"><span data-stu-id="6f3e1-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span></span>
</dt> <dd>

<span data-ttu-id="6f3e1-132">Nombre del token interno para Translator.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-132">Internal token name for translator.</span></span> <span data-ttu-id="6f3e1-133">Clave principal de la tabla.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="6f3e1-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="6f3e1-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="6f3e1-135">Clave externa en la tabla de componentes.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="6f3e1-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="6f3e1-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="6f3e1-137">Descripción registrada para este traductor de controladores ODBC.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-137">The description registered for this ODBC driver translator.</span></span> <span data-ttu-id="6f3e1-138">Este valor no se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="6f3e1-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_</span><span class="sxs-lookup"><span data-stu-id="6f3e1-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="6f3e1-140">El archivo DLL para la transferencia que se muestra en la columna Translator.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-140">The DLL file for the transfer listed in the Translator column.</span></span> <span data-ttu-id="6f3e1-141">La columna de archivo \_ es una clave externa de la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="6f3e1-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="6f3e1-142">El nombre de archivo especificado en la columna FILENAME de ese registro de tabla de archivos debe estar en el formato de nombre de archivo corto.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="6f3e1-143">No se \| puede usar la sintaxis de LFN de SFN.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="6f3e1-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuración de archivos \_</span><span class="sxs-lookup"><span data-stu-id="6f3e1-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="6f3e1-145">El archivo DLL de instalación del traductor si es diferente de la columna Translator.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-145">The setup DLL file for the translator if it is different from the Translator column.</span></span> <span data-ttu-id="6f3e1-146">La columna de archivo \_ es una clave externa de la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="6f3e1-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="6f3e1-147">El nombre de archivo especificado en la columna FILENAME de ese registro de tabla de archivos debe estar en el formato de nombre de archivo corto.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="6f3e1-148">No se \| puede usar la sintaxis de LFN de SFN.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f3e1-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f3e1-149">Remarks</span></span>

<span data-ttu-id="6f3e1-150">Las acciones [InstallODBC](installodbc-action.md) y [RemoveODBC](removeodbc-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="6f3e1-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="6f3e1-151">Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="6f3e1-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="6f3e1-152">Validación</span><span class="sxs-lookup"><span data-stu-id="6f3e1-152">Validation</span></span>

<dl>

[<span data-ttu-id="6f3e1-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="6f3e1-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6f3e1-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="6f3e1-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6f3e1-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="6f3e1-155">ICE32</span></span>](ice32.md)  
</dl>

 

 



