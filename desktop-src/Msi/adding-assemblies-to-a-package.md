---
description: Windows Installer los desarrolladores pueden usar las instrucciones de este tema para crear Windows Installer paquetes que contienen ensamblados.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Agregar ensamblados a un paquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded0795003ae8faf1b7bb945671990767d3eefb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276533"
---
# <a name="adding-assemblies-to-a-package"></a><span data-ttu-id="74cd2-103">Agregar ensamblados a un paquete</span><span class="sxs-lookup"><span data-stu-id="74cd2-103">Adding Assemblies to a Package</span></span>

<span data-ttu-id="74cd2-104">Windows Installer los desarrolladores pueden usar las instrucciones de este tema para crear Windows Installer paquetes que contienen ensamblados.</span><span class="sxs-lookup"><span data-stu-id="74cd2-104">Windows Installer developers can use the guidelines in this topic to author Windows Installer packages that contain assemblies.</span></span>

<span data-ttu-id="74cd2-105">Las siguientes directrices se aplican a los ensamblados Win32 y a los ensamblados que utiliza el Common Language Runtime de Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="74cd2-105">The following guidelines apply to Win32 assemblies, and assemblies that the common language runtime of the Microsoft .NET Framework uses.</span></span>

-   <span data-ttu-id="74cd2-106">Un componente Windows Installer no debe contener más de un ensamblado.</span><span class="sxs-lookup"><span data-stu-id="74cd2-106">A Windows Installer component should contain no more than one assembly.</span></span>
-   <span data-ttu-id="74cd2-107">Todos los archivos del ensamblado deben estar en un único componente.</span><span class="sxs-lookup"><span data-stu-id="74cd2-107">All of the files in the assembly should be in a single component.</span></span>
-   <span data-ttu-id="74cd2-108">Cada componente que contiene un ensamblado debe tener una entrada en la tabla [MsiAssembly](msiassembly-table.md) .</span><span class="sxs-lookup"><span data-stu-id="74cd2-108">Each component that contains an assembly should have an entry in the [MsiAssembly](msiassembly-table.md) table.</span></span>
-   <span data-ttu-id="74cd2-109">El nombre seguro de la caché de ensamblados de cada ensamblado se debe crear en la tabla [MsiAssemblyName](msiassemblyname-table.md) .</span><span class="sxs-lookup"><span data-stu-id="74cd2-109">The strong assembly cache name of each assembly should be authored into the [MsiAssemblyName](msiassemblyname-table.md) table.</span></span>
-   <span data-ttu-id="74cd2-110">Utilice la tabla [del registro](registry-table.md) en lugar de la tabla de [clase](class-table.md) al registrar la interoperabilidad com para un ensamblado.</span><span class="sxs-lookup"><span data-stu-id="74cd2-110">Use the [Registry](registry-table.md) table instead of the [Class](class-table.md) table when you register COM Interop for an assembly.</span></span>
-   <span data-ttu-id="74cd2-111">Los ensamblados que tienen el mismo nombre seguro son el mismo ensamblado.</span><span class="sxs-lookup"><span data-stu-id="74cd2-111">Assemblies that have the same strong name are the same assembly.</span></span> <span data-ttu-id="74cd2-112">Cuando diferentes aplicaciones instalan el mismo ensamblado, los componentes que contienen el ensamblado deben usar el mismo valor para el ComponentId en sus tablas de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="74cd2-112">When the same assembly is installed by different applications, the components that contain the assembly should use the same value for the ComponentId in their [Component](component-table.md) tables.</span></span>

> [!Note]  
> <span data-ttu-id="74cd2-113">Los anuncios de productos identifican los ensamblados que pueden instalarse y usarse en distintas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="74cd2-113">Product advertisements identify assemblies that can be installed and used by different applications.</span></span> <span data-ttu-id="74cd2-114">Los anuncios de productos no identifican ensamblados privados.</span><span class="sxs-lookup"><span data-stu-id="74cd2-114">Product advertisements do not identify private assemblies.</span></span>

 

## <a name="adding-win32-assemblies"></a><span data-ttu-id="74cd2-115">Agregar ensamblados Win32</span><span class="sxs-lookup"><span data-stu-id="74cd2-115">Adding Win32 Assemblies</span></span>

<span data-ttu-id="74cd2-116">Utilice las siguientes directrices al incluir ensamblados Win32:</span><span class="sxs-lookup"><span data-stu-id="74cd2-116">Use the following guidelines when you include Win32 assemblies:</span></span>

-   <span data-ttu-id="74cd2-117">El valor de ruta de rutas de la tabla de [componentes](component-table.md) para un componente que contiene un ensamblado Win32 no debe ser null.</span><span class="sxs-lookup"><span data-stu-id="74cd2-117">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly should not be Null.</span></span>
-   <span data-ttu-id="74cd2-118">El valor de ruta de acceso de la tabla de [componentes](component-table.md) para un componente que contiene un ensamblado de directiva Win32 debe ser el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="74cd2-118">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 policy assembly should be the manifest file.</span></span>
-   <span data-ttu-id="74cd2-119">El valor de ruta de acceso de la tabla de [componentes](component-table.md) para un componente que contiene un ensamblado de Win32, que no es un ensamblado de Directiva, no debe ser el archivo de manifiesto o el archivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="74cd2-119">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly, that is not a policy assembly, should not be the manifest file or catalog file.</span></span> <span data-ttu-id="74cd2-120">Debe ser un archivo diferente en el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="74cd2-120">It should be a different file in the assembly.</span></span>
-   <span data-ttu-id="74cd2-121">Agregue una fila a la tabla [MsiAssemblyName](msiassemblyname-table.md) para cada par de nombre y valor que se enumeran en la sección **assemblyIdentity** del manifiesto del ensamblado Win32.</span><span class="sxs-lookup"><span data-stu-id="74cd2-121">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each name and value pair that are listed in the **assemblyIdentity** section of the Win32 assembly's manifest.</span></span>

## <a name="adding-assemblies-used-with-the-net-framework"></a><span data-ttu-id="74cd2-122">Agregar ensamblados utilizados con el .NET Framework</span><span class="sxs-lookup"><span data-stu-id="74cd2-122">Adding Assemblies used with the .NET Framework</span></span>

<span data-ttu-id="74cd2-123">Utilice las siguientes directrices al incluir ensamblados que utiliza el Common Language Runtime de la .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="74cd2-123">Use the following guidelines when you include assemblies that the common language runtime of the .NET Framework uses.</span></span>

-   <span data-ttu-id="74cd2-124">El valor de ruta de rutas de la tabla de [componentes](component-table.md) para un componente que contiene el ensamblado no debe ser null.</span><span class="sxs-lookup"><span data-stu-id="74cd2-124">The KeyPath value in the [Component](component-table.md) table for a component that contains the assembly should not be Null.</span></span>
-   <span data-ttu-id="74cd2-125">Al instalar un ensamblado utilizado por el Common Language Runtime en la caché global de ensamblados, el valor de la \_ columna aplicación de archivo de la tabla MsiAssembly debe ser null.</span><span class="sxs-lookup"><span data-stu-id="74cd2-125">When you install an assembly used by the common language runtime to the global assembly cache, the value in the File\_Application column of the MsiAssembly table must be Null.</span></span>
-   <span data-ttu-id="74cd2-126">Agregue una fila a la tabla [MsiAssemblyName](msiassemblyname-table.md) para cada atributo del nombre seguro del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="74cd2-126">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each attribute of the assembly's strong name.</span></span> <span data-ttu-id="74cd2-127">Todos los ensamblados deben tener el nombre, la versión y los atributos de referencia cultural que se especifican en la tabla MsiAssemblyName.</span><span class="sxs-lookup"><span data-stu-id="74cd2-127">All assemblies must have the Name, Version, and Culture attributes that are specified in the MsiAssemblyName table.</span></span> <span data-ttu-id="74cd2-128">Se requiere un atributo publicKeyToken para un ensamblado global.</span><span class="sxs-lookup"><span data-stu-id="74cd2-128">A publicKeyToken attribute is required for a global assembly.</span></span> <span data-ttu-id="74cd2-129">La tabla siguiente es un ejemplo de la tabla MsiAssemblyName para un ensamblado global que usa el Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="74cd2-129">The following table is an example of the MsiAssemblyName table for a global assembly for use by the common language runtime.</span></span>

[<span data-ttu-id="74cd2-130">Tabla MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="74cd2-130">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)



| <span data-ttu-id="74cd2-131">Componente</span><span class="sxs-lookup"><span data-stu-id="74cd2-131">Component</span></span>  | <span data-ttu-id="74cd2-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="74cd2-132">Name</span></span>           | <span data-ttu-id="74cd2-133">Value</span><span class="sxs-lookup"><span data-stu-id="74cd2-133">Value</span></span>            |
|------------|----------------|------------------|
| <span data-ttu-id="74cd2-134">Componentea</span><span class="sxs-lookup"><span data-stu-id="74cd2-134">ComponentA</span></span> | <span data-ttu-id="74cd2-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="74cd2-135">Name</span></span>           | <span data-ttu-id="74cd2-136">simple</span><span class="sxs-lookup"><span data-stu-id="74cd2-136">simple</span></span>           |
| <span data-ttu-id="74cd2-137">Componentea</span><span class="sxs-lookup"><span data-stu-id="74cd2-137">ComponentA</span></span> | <span data-ttu-id="74cd2-138">version</span><span class="sxs-lookup"><span data-stu-id="74cd2-138">version</span></span>        | <span data-ttu-id="74cd2-139">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="74cd2-139">1.0.0.0</span></span>          |
| <span data-ttu-id="74cd2-140">Componentea</span><span class="sxs-lookup"><span data-stu-id="74cd2-140">ComponentA</span></span> | <span data-ttu-id="74cd2-141">Referencia cultural</span><span class="sxs-lookup"><span data-stu-id="74cd2-141">Culture</span></span>        | <span data-ttu-id="74cd2-142">neutral</span><span class="sxs-lookup"><span data-stu-id="74cd2-142">neutral</span></span>          |
| <span data-ttu-id="74cd2-143">Componentea</span><span class="sxs-lookup"><span data-stu-id="74cd2-143">ComponentA</span></span> | <span data-ttu-id="74cd2-144">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="74cd2-144">publicKeyToken</span></span> | <span data-ttu-id="74cd2-145">9d1ec8380f483f5a</span><span class="sxs-lookup"><span data-stu-id="74cd2-145">9d1ec8380f483f5a</span></span> |



 

 

 



