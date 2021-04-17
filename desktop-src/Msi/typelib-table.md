---
description: La tabla TypeLib contiene la información que debe colocarse en el registro del registro de las bibliotecas de tipos.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: Tabla TypeLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0aa8949df75162ffb7107b633ab766d276c4b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652361"
---
# <a name="typelib-table"></a><span data-ttu-id="bb584-103">Tabla TypeLib</span><span class="sxs-lookup"><span data-stu-id="bb584-103">TypeLib Table</span></span>

<span data-ttu-id="bb584-104">La tabla TypeLib contiene la información que debe colocarse en el registro del registro de las bibliotecas de tipos.</span><span class="sxs-lookup"><span data-stu-id="bb584-104">The TypeLib table contains the information that needs to be placed in the registry registration of type libraries.</span></span>

<span data-ttu-id="bb584-105">La tabla TypeLib tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="bb584-105">The TypeLib table has the following columns.</span></span>



| <span data-ttu-id="bb584-106">Columna</span><span class="sxs-lookup"><span data-stu-id="bb584-106">Column</span></span>      | <span data-ttu-id="bb584-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb584-107">Type</span></span>                               | <span data-ttu-id="bb584-108">Clave</span><span class="sxs-lookup"><span data-stu-id="bb584-108">Key</span></span> | <span data-ttu-id="bb584-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="bb584-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="bb584-110">LibID</span><span class="sxs-lookup"><span data-stu-id="bb584-110">LibID</span></span>       | [<span data-ttu-id="bb584-111">GUID</span><span class="sxs-lookup"><span data-stu-id="bb584-111">GUID</span></span>](guid.md)                   | <span data-ttu-id="bb584-112">Y</span><span class="sxs-lookup"><span data-stu-id="bb584-112">Y</span></span>   | <span data-ttu-id="bb584-113">N</span><span class="sxs-lookup"><span data-stu-id="bb584-113">N</span></span>        |
| <span data-ttu-id="bb584-114">Idioma</span><span class="sxs-lookup"><span data-stu-id="bb584-114">Language</span></span>    | [<span data-ttu-id="bb584-115">Entero</span><span class="sxs-lookup"><span data-stu-id="bb584-115">Integer</span></span>](integer.md)             | <span data-ttu-id="bb584-116">Y</span><span class="sxs-lookup"><span data-stu-id="bb584-116">Y</span></span>   | <span data-ttu-id="bb584-117">N</span><span class="sxs-lookup"><span data-stu-id="bb584-117">N</span></span>        |
| <span data-ttu-id="bb584-118">Componente\_</span><span class="sxs-lookup"><span data-stu-id="bb584-118">Component\_</span></span> | [<span data-ttu-id="bb584-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="bb584-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="bb584-120">Y</span><span class="sxs-lookup"><span data-stu-id="bb584-120">Y</span></span>   | <span data-ttu-id="bb584-121">N</span><span class="sxs-lookup"><span data-stu-id="bb584-121">N</span></span>        |
| <span data-ttu-id="bb584-122">Versión</span><span class="sxs-lookup"><span data-stu-id="bb584-122">Version</span></span>     | [<span data-ttu-id="bb584-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="bb584-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="bb584-124">N</span><span class="sxs-lookup"><span data-stu-id="bb584-124">N</span></span>   | <span data-ttu-id="bb584-125">Y</span><span class="sxs-lookup"><span data-stu-id="bb584-125">Y</span></span>        |
| <span data-ttu-id="bb584-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb584-126">Description</span></span> | [<span data-ttu-id="bb584-127">Texto</span><span class="sxs-lookup"><span data-stu-id="bb584-127">Text</span></span>](text.md)                   | <span data-ttu-id="bb584-128">N</span><span class="sxs-lookup"><span data-stu-id="bb584-128">N</span></span>   | <span data-ttu-id="bb584-129">Y</span><span class="sxs-lookup"><span data-stu-id="bb584-129">Y</span></span>        |
| <span data-ttu-id="bb584-130">Directorio\_</span><span class="sxs-lookup"><span data-stu-id="bb584-130">Directory\_</span></span> | [<span data-ttu-id="bb584-131">Identificador</span><span class="sxs-lookup"><span data-stu-id="bb584-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="bb584-132">N</span><span class="sxs-lookup"><span data-stu-id="bb584-132">N</span></span>   | <span data-ttu-id="bb584-133">Y</span><span class="sxs-lookup"><span data-stu-id="bb584-133">Y</span></span>        |
| <span data-ttu-id="bb584-134">Característica\_</span><span class="sxs-lookup"><span data-stu-id="bb584-134">Feature\_</span></span>   | [<span data-ttu-id="bb584-135">Identificador</span><span class="sxs-lookup"><span data-stu-id="bb584-135">Identifier</span></span>](identifier.md)       | <span data-ttu-id="bb584-136">N</span><span class="sxs-lookup"><span data-stu-id="bb584-136">N</span></span>   | <span data-ttu-id="bb584-137">N</span><span class="sxs-lookup"><span data-stu-id="bb584-137">N</span></span>        |
| <span data-ttu-id="bb584-138">Costos</span><span class="sxs-lookup"><span data-stu-id="bb584-138">Cost</span></span>        | [<span data-ttu-id="bb584-139">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="bb584-139">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="bb584-140">N</span><span class="sxs-lookup"><span data-stu-id="bb584-140">N</span></span>   | <span data-ttu-id="bb584-141">Y</span><span class="sxs-lookup"><span data-stu-id="bb584-141">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="bb584-142">Columnas</span><span class="sxs-lookup"><span data-stu-id="bb584-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="bb584-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID</span><span class="sxs-lookup"><span data-stu-id="bb584-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID</span></span>
</dt> <dd>

<span data-ttu-id="bb584-144">GUID que identifica la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="bb584-144">The GUID that identifies the library.</span></span>

</dd> <dt>

<span data-ttu-id="bb584-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Módulo</span><span class="sxs-lookup"><span data-stu-id="bb584-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="bb584-146">Lenguaje de la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="bb584-146">The language of the type library.</span></span> <span data-ttu-id="bb584-147">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="bb584-147">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="bb584-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="bb584-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="bb584-149">Clave externa en la primera columna de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="bb584-149">External key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="bb584-150">Esta columna identifica el componente que pertenece a la característica \_ cuyo archivo de clave es la biblioteca de tipos que se está registrando.</span><span class="sxs-lookup"><span data-stu-id="bb584-150">This column identifies the component belonging to Feature\_ whose key file is the type library being registered.</span></span>

</dd> <dt>

<span data-ttu-id="bb584-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versión</span><span class="sxs-lookup"><span data-stu-id="bb584-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="bb584-152">Esta es la versión de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="bb584-152">This is the version of the library.</span></span> <span data-ttu-id="bb584-153">Las versiones principal y secundaria se codifican en el valor entero de cuatro bytes.</span><span class="sxs-lookup"><span data-stu-id="bb584-153">The major and minor versions are encoded in the four byte integer value.</span></span> <span data-ttu-id="bb584-154">La versión secundaria está en los ocho bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="bb584-154">The minor version is in the lower eight bits.</span></span> <span data-ttu-id="bb584-155">La versión principal está en el medio de dieciséis bits.</span><span class="sxs-lookup"><span data-stu-id="bb584-155">The major version is in the middle sixteen bits.</span></span>

</dd> <dt>

<span data-ttu-id="bb584-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="bb584-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="bb584-157">Una descripción localizable de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="bb584-157">A localizable description of the library.</span></span>

</dd> <dt>

<span data-ttu-id="bb584-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_</span><span class="sxs-lookup"><span data-stu-id="bb584-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="bb584-159">Clave externa en la primera columna de la [tabla de directorio](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="bb584-159">External key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="bb584-160">Esta columna identifica la ruta de ayuda de la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="bb584-160">This column identifies the Help path for the type library.</span></span> <span data-ttu-id="bb584-161">Esta columna se omite durante la publicidad.</span><span class="sxs-lookup"><span data-stu-id="bb584-161">This column is ignored during advertising.</span></span>

</dd> <dt>

<span data-ttu-id="bb584-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_</span><span class="sxs-lookup"><span data-stu-id="bb584-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="bb584-163">Clave externa en la primera columna de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="bb584-163">External key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="bb584-164">Esta columna especifica la característica que se debe instalar para que la biblioteca de tipos esté operativa.</span><span class="sxs-lookup"><span data-stu-id="bb584-164">This column specifies the feature that must be installed for the type library to be operational.</span></span>

</dd> <dt>

<span data-ttu-id="bb584-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Costará</span><span class="sxs-lookup"><span data-stu-id="bb584-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="bb584-166">Costo asociado al registro de la biblioteca de tipos en bytes.</span><span class="sxs-lookup"><span data-stu-id="bb584-166">The cost associated with the registration of the type library in bytes.</span></span> <span data-ttu-id="bb584-167">Debe ser un número no negativo o null.</span><span class="sxs-lookup"><span data-stu-id="bb584-167">This must be a non-negative number or null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb584-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb584-168">Remarks</span></span>

<span data-ttu-id="bb584-169">Se hace referencia a esta tabla cuando se ejecuta la acción [RegisterTypeLibraries](registertypelibraries-action.md) o la [acción UnregisterTypeLibraries](unregistertypelibraries-action.md) .</span><span class="sxs-lookup"><span data-stu-id="bb584-169">This table is referred to when the [RegisterTypeLibraries action](registertypelibraries-action.md) or the [UnregisterTypeLibraries action](unregistertypelibraries-action.md) is executed.</span></span>

<span data-ttu-id="bb584-170">El instalador escribe toda la información de registro de la biblioteca de tipos en la \_ \_ Ubicación del registro HKEY local Machine (HKLM).</span><span class="sxs-lookup"><span data-stu-id="bb584-170">The installer writes all type library registration information into the HKEY\_LOCAL\_MACHINE (HKLM) registry location.</span></span> <span data-ttu-id="bb584-171">Este es el caso incluso en las instalaciones por usuario.</span><span class="sxs-lookup"><span data-stu-id="bb584-171">This is the case even for per-user installations.</span></span> <span data-ttu-id="bb584-172">Las bibliotecas de tipos no se pueden registrar en ubicaciones por usuario (HKCU).</span><span class="sxs-lookup"><span data-stu-id="bb584-172">Type libraries cannot be registered in per-user locations (HKCU).</span></span>

<span data-ttu-id="bb584-173">Se recomienda encarecidamente a los autores de paquetes de instalación que utilicen la tabla TypeLib.</span><span class="sxs-lookup"><span data-stu-id="bb584-173">Installation package authors are strongly advised against using the TypeLib table.</span></span> <span data-ttu-id="bb584-174">En su lugar, deben registrar las bibliotecas de tipos mediante la tabla [del registro](registry-table.md) .</span><span class="sxs-lookup"><span data-stu-id="bb584-174">Instead, they should register type libraries by using the [Registry](registry-table.md) table.</span></span> <span data-ttu-id="bb584-175">Entre los motivos para evitar el registro propio se incluyen:</span><span class="sxs-lookup"><span data-stu-id="bb584-175">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="bb584-176">Si se produce un error en una instalación con la tabla TypeLib y se debe revertir, es posible que la reversión no restaure el equipo al mismo estado que existía antes de la reversión.</span><span class="sxs-lookup"><span data-stu-id="bb584-176">If an installation using the TypeLib table fails and must be rolled back, the rollback may not restore the computer to the same state that existed prior to the rollback.</span></span> <span data-ttu-id="bb584-177">Es posible que las bibliotecas de tipos registradas antes de la reversión no se registren después de la reversión.</span><span class="sxs-lookup"><span data-stu-id="bb584-177">Type libraries registered prior to rollback may not be registered after rollback.</span></span>

## <a name="validation"></a><span data-ttu-id="bb584-178">Validación</span><span class="sxs-lookup"><span data-stu-id="bb584-178">Validation</span></span>

<dl>

[<span data-ttu-id="bb584-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="bb584-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="bb584-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="bb584-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="bb584-181">ICE19</span><span class="sxs-lookup"><span data-stu-id="bb584-181">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="bb584-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="bb584-182">ICE32</span></span>](ice32.md)  
</dl>

 

 



