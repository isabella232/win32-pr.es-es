---
description: En el procedimiento siguiente se describen los pasos generales para crear módulos de combinación.
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: Crear módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276517"
---
# <a name="authoring-merge-modules"></a><span data-ttu-id="9b118-103">Crear módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-103">Authoring Merge Modules</span></span>

<span data-ttu-id="9b118-104">En el procedimiento siguiente se describen los pasos generales para crear módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="9b118-104">The following procedure describes the general steps to authoring merge modules.</span></span>

<span data-ttu-id="9b118-105">**Para crear un nuevo módulo de combinación**</span><span class="sxs-lookup"><span data-stu-id="9b118-105">**To create a new merge module**</span></span>

1.  <span data-ttu-id="9b118-106">Obtenga una herramienta de software que puede utilizar para editar la base de datos del módulo de fusión mediante combinación.</span><span class="sxs-lookup"><span data-stu-id="9b118-106">Obtain a software tool you can use to edit the merge module database.</span></span>
2.  <span data-ttu-id="9b118-107">Obtener una base de datos de módulo de mezcla en blanco.</span><span class="sxs-lookup"><span data-stu-id="9b118-107">Obtain a blank merge module database.</span></span>
3.  <span data-ttu-id="9b118-108">Genere un [GUID](guid.md) para el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="9b118-108">Generate a [GUID](guid.md) for the merge module.</span></span> <span data-ttu-id="9b118-109">Debe usar este GUID al crear las claves principales de las tablas de base de datos en el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="9b118-109">You need to use this GUID when authoring the primary keys of database tables in the merge module.</span></span>
4.  <span data-ttu-id="9b118-110">Agregue un registro a la [tabla de componentes](component-table.md) para cada componente entregado por la combinación.</span><span class="sxs-lookup"><span data-stu-id="9b118-110">Add a record to the [Component table](component-table.md) for each component delivered by the merge.</span></span> <span data-ttu-id="9b118-111">En cada módulo de combinación se requiere una tabla de componentes.</span><span class="sxs-lookup"><span data-stu-id="9b118-111">A Component table is required in every merge module.</span></span> <span data-ttu-id="9b118-112">Tenga en cuenta que los módulos de combinación operan con componentes y no con características.</span><span class="sxs-lookup"><span data-stu-id="9b118-112">Note that merge modules operate with components and not with features.</span></span> <span data-ttu-id="9b118-113">Sin embargo, en algunos casos, es posible que una entrada de la tabla de base de datos tenga que hacer referencia a una característica.</span><span class="sxs-lookup"><span data-stu-id="9b118-113">In certain cases, however, a database table entry may need to reference a feature.</span></span> <span data-ttu-id="9b118-114">Para obtener más información, vea [hacer referencia a características en módulos de combinación](referencing-features-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="9b118-114">For details, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>
5.  <span data-ttu-id="9b118-115">Agregue una [tabla de directorio](directory-table.md) al módulo de combinación que especifique el diseño de los directorios que el módulo de combinación agrega a la base de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="9b118-115">Add a [Directory table](directory-table.md) to the merge module that specifies the layout of directories the merge module adds to the target database.</span></span> <span data-ttu-id="9b118-116">Se requiere una tabla de directorio en cada módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="9b118-116">A Directory table is required in every merge module.</span></span>
6.  <span data-ttu-id="9b118-117">Importe una [tabla FeatureComponents](featurecomponents-table.md) en blanco en la base de datos del módulo de fusión mediante combinación.</span><span class="sxs-lookup"><span data-stu-id="9b118-117">Import a blank [FeatureComponents table](featurecomponents-table.md) into the merge module database.</span></span> <span data-ttu-id="9b118-118">Esta tabla vacía proporciona una guía para la herramienta de combinación en los casos en los que el archivo. msi no contiene su propia tabla FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="9b118-118">This empty table provides a guideline for the merge tool in cases where the .msi file does not contain its own FeatureComponents table.</span></span>
7.  <span data-ttu-id="9b118-119">Recopile todos los archivos entregados por este módulo de combinación y cree el archivo. cab de [MergeModule.CABinet](mergemodule-cabinet.md) .</span><span class="sxs-lookup"><span data-stu-id="9b118-119">Collect all the files delivered by this merge module and create the [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file.</span></span> <span data-ttu-id="9b118-120">Agregue el archivo. cab al módulo de combinación como una secuencia dentro del archivo. msm.</span><span class="sxs-lookup"><span data-stu-id="9b118-120">Add the cabinet to the merge module as a stream inside the .msm file.</span></span>
8.  <span data-ttu-id="9b118-121">Agregue un registro a la tabla de archivos para cada archivo almacenado en MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="9b118-121">Add a record to the File table for every file stored in MergeModule.CABinet.</span></span>
9.  <span data-ttu-id="9b118-122">Agregue la información necesaria para identificar el módulo de combinación en la [tabla ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="9b118-122">Add the information necessary to identify the merge module in the [ModuleSignature table](modulesignature-table.md).</span></span> <span data-ttu-id="9b118-123">Cada módulo de combinación requiere una tabla ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="9b118-123">Every merge module requires a ModuleSignature table.</span></span>
10. <span data-ttu-id="9b118-124">Enumere los componentes del módulo de combinación en la [tabla ModuleComponents](modulecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="9b118-124">List the components in the merge module in the [ModuleComponents table](modulecomponents-table.md).</span></span> <span data-ttu-id="9b118-125">Cada módulo de combinación requiere una tabla ModuleComponents.</span><span class="sxs-lookup"><span data-stu-id="9b118-125">Every merge module requires a ModuleComponents table.</span></span>
11. <span data-ttu-id="9b118-126">Agregue tablas de secuencia de módulo de combinación al archivo. MSM solo si el módulo de combinación debe modificar las [*tablas de secuencia*](s-gly.md) de la base de datos de instalación de destino.</span><span class="sxs-lookup"><span data-stu-id="9b118-126">Add merge module sequence tables to the .msm file only if the merge module needs to modify the [*sequence tables*](s-gly.md) of the target installation database.</span></span>
12. <span data-ttu-id="9b118-127">Agregue una \_ tabla de validación al módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="9b118-127">Add a \_Validation table to the merge module.</span></span> <span data-ttu-id="9b118-128">Un módulo de combinación requiere una \_ tabla de validación para pasar la validación.</span><span class="sxs-lookup"><span data-stu-id="9b118-128">A merge module requires a \_Validation table to pass validation.</span></span>
13. <span data-ttu-id="9b118-129">Los módulos de combinación requieren una interfaz de usuario en solo casos raros.</span><span class="sxs-lookup"><span data-stu-id="9b118-129">Merge modules require a user interface in only rare cases.</span></span> <span data-ttu-id="9b118-130">No se recomienda incluir una interfaz de usuario con un módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="9b118-130">Including a UI with a merge module is not recommended.</span></span> <span data-ttu-id="9b118-131">En los casos en los que se requiere una interfaz de usuario, las tablas de la interfaz de usuario se pueden combinar en el archivo. msi de la misma forma que otras tablas.</span><span class="sxs-lookup"><span data-stu-id="9b118-131">In cases where a user interface is required, the UI tables can be merged into the .msi file the same as other tables.</span></span>
14. <span data-ttu-id="9b118-132">Agregue información del registro a las tablas del registro adecuadas en la base de datos del módulo de mezcla.</span><span class="sxs-lookup"><span data-stu-id="9b118-132">Add registry information to the appropriate registry tables in the merge module database.</span></span> <span data-ttu-id="9b118-133">Agregue información del registro para bibliotecas de tipos, clases, extensiones y verbos a las tablas [typelib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)o [MIME](mime-table.md) .</span><span class="sxs-lookup"><span data-stu-id="9b118-133">Add registry information for type libraries, classes, extensions, and verbs into the [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="9b118-134">Toda la demás información del registro puede incluirse en la [tabla del registro](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="9b118-134">All other registry information can go into the [Registry table](registry-table.md).</span></span> <span data-ttu-id="9b118-135">No se recomienda el uso de la tabla SelfReg.</span><span class="sxs-lookup"><span data-stu-id="9b118-135">The use of the SelfReg table is not recommended.</span></span>
15. <span data-ttu-id="9b118-136">Agregue la información de resumen al [flujo de información de resumen del módulo de combinación](merge-module-summary-information-stream-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9b118-136">Add the summary information to the [Merge Module Summary Information Stream](merge-module-summary-information-stream-reference.md).</span></span>
16. <span data-ttu-id="9b118-137">Ejecute la validación en todos los módulos de combinación antes de intentar instalar.</span><span class="sxs-lookup"><span data-stu-id="9b118-137">Run validation on all merge modules before attempting to install.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b118-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b118-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b118-139">Obtener las bases de datos del módulo de combinación en blanco</span><span class="sxs-lookup"><span data-stu-id="9b118-139">Obtaining Blank Merge Module Databases</span></span>](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="9b118-140">Obtener herramientas de creación de módulos de fusión mediante combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-140">Obtaining Merge Module Authoring Tools</span></span>](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[<span data-ttu-id="9b118-141">Asignar nombres a las claves principales de las bases de datos de módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-141">Naming Primary Keys in Merge Module Databases</span></span>](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="9b118-142">Crear tablas de componentes de módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-142">Authoring Merge Module Component Tables</span></span>](authoring-merge-module-component-tables.md)
</dt> <dt>

[<span data-ttu-id="9b118-143">Crear tablas del directorio del módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-143">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="9b118-144">Crear tablas FeatureComponents de módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-144">Authoring Merge Module FeatureComponents Tables</span></span>](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="9b118-145">Generación de archivos. cab de MergeModule.CABinet</span><span class="sxs-lookup"><span data-stu-id="9b118-145">Generating MergeModule.CABinet Cabinet Files</span></span>](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[<span data-ttu-id="9b118-146">Crear tablas de archivos de módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-146">Authoring Merge Module File Tables</span></span>](authoring-merge-module-file-tables.md)
</dt> <dt>

[<span data-ttu-id="9b118-147">Creación de tablas ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="9b118-147">Authoring ModuleSignature Tables</span></span>](authoring-modulesignature-tables.md)
</dt> <dt>

[<span data-ttu-id="9b118-148">Creación de tablas ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="9b118-148">Authoring ModuleComponents Tables</span></span>](authoring-modulecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="9b118-149">Crear tablas de secuencia de módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-149">Authoring Merge Module Sequence Tables</span></span>](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[<span data-ttu-id="9b118-150">Validar módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-150">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="9b118-151">Crear interfaces de usuario en módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-151">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="9b118-152">Crear tablas del registro del módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-152">Authoring Merge Module Registry Tables</span></span>](authoring-merge-module-registry-tables.md)
</dt> <dt>

[<span data-ttu-id="9b118-153">Crear secuencias de información de resumen del módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-153">Authoring Merge Module Summary Information Streams</span></span>](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[<span data-ttu-id="9b118-154">Referencia de flujo de información de resumen del módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-154">Merge Module Summary Information Stream Reference</span></span>](merge-module-summary-information-stream-reference.md)
</dt> <dt>

<span data-ttu-id="9b118-155">Validar módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="9b118-155">Validating Merge Modules</span></span>
</dt> <dt>

[<span data-ttu-id="9b118-156">Usar módulos de combinación de 64 bits</span><span class="sxs-lookup"><span data-stu-id="9b118-156">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



