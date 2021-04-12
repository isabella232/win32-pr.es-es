---
description: ICE57 valida que los componentes individuales no mezclen los datos por equipo y por usuario. Esta acción personalizada de ICE comprueba las entradas del registro, los archivos, las rutas de acceso a las claves del directorio y los métodos abreviados no anunciados.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278157"
---
# <a name="ice57"></a><span data-ttu-id="c6314-104">ICE57</span><span class="sxs-lookup"><span data-stu-id="c6314-104">ICE57</span></span>

<span data-ttu-id="c6314-105">ICE57 valida que los componentes individuales no mezclen los datos por equipo y por usuario.</span><span class="sxs-lookup"><span data-stu-id="c6314-105">ICE57 validates that individual components do not mix per-machine and per-user data.</span></span> <span data-ttu-id="c6314-106">Esta acción personalizada de ICE comprueba las entradas del registro, los archivos, las rutas de acceso a las claves del directorio y los métodos abreviados no anunciados.</span><span class="sxs-lookup"><span data-stu-id="c6314-106">This ICE custom action checks registry entries, files, directory key paths, and non-advertised shortcuts.</span></span>

<span data-ttu-id="c6314-107">La combinación de datos por usuario y por equipo en el mismo componente podría dar lugar a la instalación parcial del componente solo para algunos usuarios en un entorno de varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="c6314-107">Mixing per-user and per-machine data in the same component could result in only partial installation of the component for some users in a multi-user environment.</span></span>

<span data-ttu-id="c6314-108">Vea la propiedad [**AllUsers**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="c6314-108">See the [**ALLUSERS**](allusers.md) property.</span></span>

## <a name="result"></a><span data-ttu-id="c6314-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="c6314-109">Result</span></span>

<span data-ttu-id="c6314-110">ICE57 publica un error si encuentra algún componente que contenga entradas de registro por equipo y por usuario, archivos, rutas de acceso de clave de directorio o accesos directos no anunciados.</span><span class="sxs-lookup"><span data-stu-id="c6314-110">ICE57 posts an error if it finds any component that contains both a per-machine and per-user registry entries, files, directory key paths, or non-advertised shortcuts.</span></span>

## <a name="example"></a><span data-ttu-id="c6314-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6314-111">Example</span></span>

<span data-ttu-id="c6314-112">ICE57reports los siguientes errores para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="c6314-112">ICE57reports the following errors for the example shown.</span></span>

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

<span data-ttu-id="c6314-113">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c6314-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="c6314-114">Componente</span><span class="sxs-lookup"><span data-stu-id="c6314-114">Component</span></span>  | <span data-ttu-id="c6314-115">Directorio</span><span class="sxs-lookup"><span data-stu-id="c6314-115">Directory</span></span>  | <span data-ttu-id="c6314-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="c6314-116">Attributes</span></span> | <span data-ttu-id="c6314-117">Rutas</span><span class="sxs-lookup"><span data-stu-id="c6314-117">KeyPath</span></span> |
|------------|------------|------------|---------|
| <span data-ttu-id="c6314-118">Component1</span><span class="sxs-lookup"><span data-stu-id="c6314-118">Component1</span></span> | <span data-ttu-id="c6314-119">Directorioa</span><span class="sxs-lookup"><span data-stu-id="c6314-119">DirectoryA</span></span> | <span data-ttu-id="c6314-120">0</span><span class="sxs-lookup"><span data-stu-id="c6314-120">0</span></span>          | <span data-ttu-id="c6314-121">Archivoa</span><span class="sxs-lookup"><span data-stu-id="c6314-121">FileA</span></span>   |
| <span data-ttu-id="c6314-122">Component2</span><span class="sxs-lookup"><span data-stu-id="c6314-122">Component2</span></span> | <span data-ttu-id="c6314-123">Directorioa</span><span class="sxs-lookup"><span data-stu-id="c6314-123">DirectoryA</span></span> | <span data-ttu-id="c6314-124">4</span><span class="sxs-lookup"><span data-stu-id="c6314-124">4</span></span>          | <span data-ttu-id="c6314-125">RegKeyB</span><span class="sxs-lookup"><span data-stu-id="c6314-125">RegKeyB</span></span> |
| <span data-ttu-id="c6314-126">Component3</span><span class="sxs-lookup"><span data-stu-id="c6314-126">Component3</span></span> | <span data-ttu-id="c6314-127">Directorioa</span><span class="sxs-lookup"><span data-stu-id="c6314-127">DirectoryA</span></span> | <span data-ttu-id="c6314-128">0</span><span class="sxs-lookup"><span data-stu-id="c6314-128">0</span></span>          | <span data-ttu-id="c6314-129">FileC</span><span class="sxs-lookup"><span data-stu-id="c6314-129">FileC</span></span>   |
| <span data-ttu-id="c6314-130">Component4</span><span class="sxs-lookup"><span data-stu-id="c6314-130">Component4</span></span> | <span data-ttu-id="c6314-131">Directorioa</span><span class="sxs-lookup"><span data-stu-id="c6314-131">DirectoryA</span></span> | <span data-ttu-id="c6314-132">4</span><span class="sxs-lookup"><span data-stu-id="c6314-132">4</span></span>          | <span data-ttu-id="c6314-133">RegKeyD</span><span class="sxs-lookup"><span data-stu-id="c6314-133">RegKeyD</span></span> |



 

<span data-ttu-id="c6314-134">[Tabla del registro](registry-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c6314-134">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="c6314-135">Registro</span><span class="sxs-lookup"><span data-stu-id="c6314-135">Registry</span></span> | <span data-ttu-id="c6314-136">Root</span><span class="sxs-lookup"><span data-stu-id="c6314-136">Root</span></span> | <span data-ttu-id="c6314-137">Componente\_</span><span class="sxs-lookup"><span data-stu-id="c6314-137">Component\_</span></span> |
|----------|------|-------------|
| <span data-ttu-id="c6314-138">RegKeyA</span><span class="sxs-lookup"><span data-stu-id="c6314-138">RegKeyA</span></span>  | <span data-ttu-id="c6314-139">1</span><span class="sxs-lookup"><span data-stu-id="c6314-139">1</span></span>    | <span data-ttu-id="c6314-140">Component1</span><span class="sxs-lookup"><span data-stu-id="c6314-140">Component1</span></span>  |
| <span data-ttu-id="c6314-141">RegKeyB</span><span class="sxs-lookup"><span data-stu-id="c6314-141">RegKeyB</span></span>  | <span data-ttu-id="c6314-142">1</span><span class="sxs-lookup"><span data-stu-id="c6314-142">1</span></span>    | <span data-ttu-id="c6314-143">Component2</span><span class="sxs-lookup"><span data-stu-id="c6314-143">Component2</span></span>  |
| <span data-ttu-id="c6314-144">RegKeyC</span><span class="sxs-lookup"><span data-stu-id="c6314-144">RegKeyC</span></span>  | <span data-ttu-id="c6314-145">-1</span><span class="sxs-lookup"><span data-stu-id="c6314-145">-1</span></span>   | <span data-ttu-id="c6314-146">Component3</span><span class="sxs-lookup"><span data-stu-id="c6314-146">Component3</span></span>  |
| <span data-ttu-id="c6314-147">RegKeyD</span><span class="sxs-lookup"><span data-stu-id="c6314-147">RegKeyD</span></span>  | <span data-ttu-id="c6314-148">-1</span><span class="sxs-lookup"><span data-stu-id="c6314-148">-1</span></span>   | <span data-ttu-id="c6314-149">Component4</span><span class="sxs-lookup"><span data-stu-id="c6314-149">Component4</span></span>  |



 

<span data-ttu-id="c6314-150">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c6314-150">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="c6314-151">Archivo</span><span class="sxs-lookup"><span data-stu-id="c6314-151">File</span></span>  | <span data-ttu-id="c6314-152">Componente\_</span><span class="sxs-lookup"><span data-stu-id="c6314-152">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="c6314-153">Archivoa</span><span class="sxs-lookup"><span data-stu-id="c6314-153">FileA</span></span> | <span data-ttu-id="c6314-154">Component1</span><span class="sxs-lookup"><span data-stu-id="c6314-154">Component1</span></span>  |
| <span data-ttu-id="c6314-155">FileB</span><span class="sxs-lookup"><span data-stu-id="c6314-155">FileB</span></span> | <span data-ttu-id="c6314-156">Component2</span><span class="sxs-lookup"><span data-stu-id="c6314-156">Component2</span></span>  |
| <span data-ttu-id="c6314-157">FileC</span><span class="sxs-lookup"><span data-stu-id="c6314-157">FileC</span></span> | <span data-ttu-id="c6314-158">Component3</span><span class="sxs-lookup"><span data-stu-id="c6314-158">Component3</span></span>  |
| <span data-ttu-id="c6314-159">Registrado</span><span class="sxs-lookup"><span data-stu-id="c6314-159">FileD</span></span> | <span data-ttu-id="c6314-160">Component4</span><span class="sxs-lookup"><span data-stu-id="c6314-160">Component4</span></span>  |



 

[<span data-ttu-id="c6314-161">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="c6314-161">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="c6314-162">Directorio</span><span class="sxs-lookup"><span data-stu-id="c6314-162">Directory</span></span>  | <span data-ttu-id="c6314-163">Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="c6314-163">Directory\_Parent</span></span> | <span data-ttu-id="c6314-164">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="c6314-164">DefaultDir</span></span> |
|------------|-------------------|------------|
| <span data-ttu-id="c6314-165">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="c6314-165">TARGETDIR</span></span>  |                   | <span data-ttu-id="c6314-166">SourceDir</span><span class="sxs-lookup"><span data-stu-id="c6314-166">SourceDir</span></span>  |
| <span data-ttu-id="c6314-167">Directorioa</span><span class="sxs-lookup"><span data-stu-id="c6314-167">DirectoryA</span></span> | <span data-ttu-id="c6314-168">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="c6314-168">TARGETDIR</span></span>         | <span data-ttu-id="c6314-169">Directorioa</span><span class="sxs-lookup"><span data-stu-id="c6314-169">DirectoryA</span></span> |



 

<span data-ttu-id="c6314-170">Para corregir los errores, reorganice la aplicación de modo que cada componente contenga solo recursos por usuario o por equipo, y no ambos.</span><span class="sxs-lookup"><span data-stu-id="c6314-170">To fix the errors, reorganize the application such that each component contains only per-user or per-machine resources, and not both.</span></span>

<span data-ttu-id="c6314-171">Se envía el primer mensaje de error porque Component1 contiene Filea (por equipo) y la clave del registro HKCU RegKeyA (por usuario).</span><span class="sxs-lookup"><span data-stu-id="c6314-171">The first error message is posted because Component1 contains FileA (per-machine) and the HKCU registry key RegKeyA (per user).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6314-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6314-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6314-173">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="c6314-173">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



