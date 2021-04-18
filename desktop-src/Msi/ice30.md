---
description: ICE30 valida que la instalación de los componentes que contienen el mismo archivo nunca instala el archivo más de una vez en el mismo directorio.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fa96899231015d864e5a0912b8ff73cedbbe75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667758"
---
# <a name="ice30"></a><span data-ttu-id="c5938-103">ICE30</span><span class="sxs-lookup"><span data-stu-id="c5938-103">ICE30</span></span>

<span data-ttu-id="c5938-104">ICE30 valida que la instalación de los componentes que contienen el mismo archivo nunca instala el archivo más de una vez en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="c5938-104">ICE30 validates that the installation of components containing the same file never installs the file more than once in the same directory.</span></span>

<span data-ttu-id="c5938-105">ICE30 va a todos los componentes de la [tabla componente](component-table.md) y, a continuación, determina el directorio de destino del componente en la [tabla de directorios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="c5938-105">ICE30 goes to every component in the [Component table](component-table.md) and then determines the component's target directory from the [Directory table](directory-table.md).</span></span> <span data-ttu-id="c5938-106">Después, comprueba para ver cuáles de estos componentes se instalan en el mismo directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="c5938-106">It then checks to see which of these components install to the same target directory.</span></span> <span data-ttu-id="c5938-107">Por último, usa la [tabla de archivos](file-table.md) para comprobar que ninguno de los archivos de estos componentes tiene el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="c5938-107">Finally, it uses the [File table](file-table.md) to verify that none of the files in these components have the same name.</span></span>

<span data-ttu-id="c5938-108">ICE30 comprueba los nombres de archivo largos (LFN) y los nombres de archivo cortos (SFN).</span><span class="sxs-lookup"><span data-stu-id="c5938-108">ICE30 checks both long file names (LFN) and short file names (SFN).</span></span>

<span data-ttu-id="c5938-109">ICE30 no evalúa las propiedades en la resolución de directorios porque estas propiedades pueden cambiar en tiempo de ejecución y modificar el esquema de resolución de directorios.</span><span class="sxs-lookup"><span data-stu-id="c5938-109">ICE30 does not evaluate properties in the resolution of directories because these properties can change at runtime and alter the directory resolution scheme.</span></span> <span data-ttu-id="c5938-110">Esto significa que ICE30 puede detectar colisiones de archivos debido a directorios con la misma propiedad en sus rutas de acceso, pero no detecta colisiones resultantes de dos propiedades que tienen el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="c5938-110">This means ICE30 can detect file collisions due to directories with the same property in their paths, but does not detect collisions resulting from two properties having the same value.</span></span>

## <a name="result"></a><span data-ttu-id="c5938-111">Resultado</span><span class="sxs-lookup"><span data-stu-id="c5938-111">Result</span></span>

<span data-ttu-id="c5938-112">ICE30 envía un mensaje de error para cada par de componentes que instala el mismo archivo en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="c5938-112">ICE30 posts an error message for each pair of components that installs the same file to the same directory.</span></span>

## <a name="example"></a><span data-ttu-id="c5938-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c5938-113">Example</span></span>

<span data-ttu-id="c5938-114">En el ejemplo mostrado se devuelve dos veces cada uno de los siguientes errores.</span><span class="sxs-lookup"><span data-stu-id="c5938-114">The example shown returns each of the following errors twice.</span></span>



| <span data-ttu-id="c5938-115">Error o advertencia de ICE30</span><span class="sxs-lookup"><span data-stu-id="c5938-115">ICE30 error or warning</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="c5938-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5938-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5938-117">ERROR: el archivo de destino ' README. 1o ' está instalado en ' TARGETDIR \\ Product ' por dos componentes diferentes en un sistema SFN: ' Component1 ' y ' Component2 '.</span><span class="sxs-lookup"><span data-stu-id="c5938-117">ERROR: The target file 'README.1st' is installed in 'TARGETDIR\\PRODUCT' by two different components on an SFN system: 'Component1' and 'Component2'.</span></span> <span data-ttu-id="c5938-118">Esto rompe el recuento de referencias de componentes.</span><span class="sxs-lookup"><span data-stu-id="c5938-118">This breaks component reference counting.</span></span>                                                                                           | <span data-ttu-id="c5938-119">Component1 y Component2 tienen un archivo denominado ' READEME. 1º '.</span><span class="sxs-lookup"><span data-stu-id="c5938-119">Component1 and Component2 both have a file named 'READEME.1st'.</span></span> <span data-ttu-id="c5938-120">Al usar nombres de archivo cortos, el instalador instala dir1 y Dir2 en el mismo directorio, el \\ producto targetdir.</span><span class="sxs-lookup"><span data-stu-id="c5938-120">When using short file names, the installer installs both Dir1 and Dir2 to the same directory, TARGETDIR\\PRODUCT.</span></span><br/> <span data-ttu-id="c5938-121">ICE30 genera dos errores, uno para cada archivo.</span><span class="sxs-lookup"><span data-stu-id="c5938-121">ICE30 generate two errors, one for each file.</span></span> <span data-ttu-id="c5938-122">En un entorno de creación que muestre ubicaciones de errores, el primer error se encuentra en la entrada de un archivo en la [tabla de archivos](file-table.md)y en la segunda ubicación del otro archivo.</span><span class="sxs-lookup"><span data-stu-id="c5938-122">In an authoring environment that displays error locations, the first error is at one file's entry in the [File Table](file-table.md), and the second at the location of the other file.</span></span><br/> |
| <span data-ttu-id="c5938-123">ERROR: la instalación de un componente condicional haría que el archivo de destino ' README. 1o ' se instalara en ' TARGETDIR \\ Common Tools ' por dos componentes diferentes en un sistema LFN: ' Component3 ' y ' Component4 '.</span><span class="sxs-lookup"><span data-stu-id="c5938-123">ERROR: Installation of a conditionalized component would cause the target file 'README.1st' to be installed in 'TARGETDIR\\COMMON TOOLS' by two different components on an LFN system: 'Component3' and 'Component4'.</span></span> <span data-ttu-id="c5938-124">Esto interrumpirá el recuento de referencias de componentes.</span><span class="sxs-lookup"><span data-stu-id="c5938-124">This would break component reference counting.</span></span>                      | <span data-ttu-id="c5938-125">Component4 tiene una entrada en la columna condition de la [tabla Component](component-table.md) y Component3 no.</span><span class="sxs-lookup"><span data-stu-id="c5938-125">Component4 has an entry in the Condition column of the [Component table](component-table.md) and Component3 does not.</span></span> <span data-ttu-id="c5938-126">Si [**VersionNT**](versionnt.md) es true, se instala Component4 y existe una colisión con el archivo Léame. 1ª siempre instalado por Component3.</span><span class="sxs-lookup"><span data-stu-id="c5938-126">If [**VersionNT**](versionnt.md) is True, Component4 is installed, and there a collision with the Readme.1st always installed by Component3.</span></span><br/> <span data-ttu-id="c5938-127">ICE30 genera 4 errores, un par para SFN, uno para LFN.</span><span class="sxs-lookup"><span data-stu-id="c5938-127">ICE30 generates 4 errors, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |
| <span data-ttu-id="c5938-128">ADVERTENCIA: el archivo de destino ' README. 1o ' puede instalarse en ' TARGETDIR \\ Common Tools ' mediante dos componentes condicionales diferentes en un sistema SFN: ' Component4 ' y ' Component5 '.</span><span class="sxs-lookup"><span data-stu-id="c5938-128">WARNING: The target file 'README.1st' might be installed in 'TARGETDIR\\COMMON TOOLS' by two different conditionalized components on an SFN system: 'Component4' and 'Component5'.</span></span> <span data-ttu-id="c5938-129">Si las condiciones no son mutuamente excluyentes, se interrumpirá el sistema de recuento de referencias de componentes.</span><span class="sxs-lookup"><span data-stu-id="c5938-129">If the conditions are not mutually exclusive, this will break the component reference counting system.</span></span> | <span data-ttu-id="c5938-130">Dado que Component4 y Component5 tienen entradas en la columna condición de la [tabla componente](component-table.md) , esta colisión de archivos puede no producirse.</span><span class="sxs-lookup"><span data-stu-id="c5938-130">Because Component4 and Component5 both have entries in the Condition column of the [Component table](component-table.md) this file collision may not occur.</span></span> <span data-ttu-id="c5938-131">ICE30 solo publica una advertencia porque las condiciones deben determinarse en el momento de la instalación.</span><span class="sxs-lookup"><span data-stu-id="c5938-131">ICE30 only posts a warning because the conditions must be determined at the time of the installation.</span></span><br/> <span data-ttu-id="c5938-132">ICE30 genera 4 Advertencias, una par para SFN, una para LFN.</span><span class="sxs-lookup"><span data-stu-id="c5938-132">ICE30 generates 4 warnings, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |



 

<span data-ttu-id="c5938-133">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c5938-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="c5938-134">Componente</span><span class="sxs-lookup"><span data-stu-id="c5938-134">Component</span></span>  | <span data-ttu-id="c5938-135">Directorio</span><span class="sxs-lookup"><span data-stu-id="c5938-135">Directory</span></span> | <span data-ttu-id="c5938-136">Condición</span><span class="sxs-lookup"><span data-stu-id="c5938-136">Condition</span></span> |
|------------|-----------|-----------|
| <span data-ttu-id="c5938-137">Component1</span><span class="sxs-lookup"><span data-stu-id="c5938-137">Component1</span></span> | <span data-ttu-id="c5938-138">Dir1</span><span class="sxs-lookup"><span data-stu-id="c5938-138">Dir1</span></span>      |           |
| <span data-ttu-id="c5938-139">Component2</span><span class="sxs-lookup"><span data-stu-id="c5938-139">Component2</span></span> | <span data-ttu-id="c5938-140">Dir2</span><span class="sxs-lookup"><span data-stu-id="c5938-140">Dir2</span></span>      |           |
| <span data-ttu-id="c5938-141">Component3</span><span class="sxs-lookup"><span data-stu-id="c5938-141">Component3</span></span> | <span data-ttu-id="c5938-142">Dir3</span><span class="sxs-lookup"><span data-stu-id="c5938-142">Dir3</span></span>      |           |
| <span data-ttu-id="c5938-143">Component4</span><span class="sxs-lookup"><span data-stu-id="c5938-143">Component4</span></span> | <span data-ttu-id="c5938-144">Dir3</span><span class="sxs-lookup"><span data-stu-id="c5938-144">Dir3</span></span>      | <span data-ttu-id="c5938-145">VersionNT</span><span class="sxs-lookup"><span data-stu-id="c5938-145">VersionNT</span></span> |
| <span data-ttu-id="c5938-146">Component5</span><span class="sxs-lookup"><span data-stu-id="c5938-146">Component5</span></span> | <span data-ttu-id="c5938-147">Dir3</span><span class="sxs-lookup"><span data-stu-id="c5938-147">Dir3</span></span>      | <span data-ttu-id="c5938-148">Version9X</span><span class="sxs-lookup"><span data-stu-id="c5938-148">Version9X</span></span> |



 

[<span data-ttu-id="c5938-149">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="c5938-149">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="c5938-150">Directorio</span><span class="sxs-lookup"><span data-stu-id="c5938-150">Directory</span></span> | <span data-ttu-id="c5938-151">\_Directorio principal</span><span class="sxs-lookup"><span data-stu-id="c5938-151">Parent\_Directory</span></span> | <span data-ttu-id="c5938-152">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="c5938-152">DefaultDir</span></span>                    |
|-----------|-------------------|-------------------------------|
| <span data-ttu-id="c5938-153">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="c5938-153">SOURCEDIR</span></span> |                   | <span data-ttu-id="c5938-154">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="c5938-154">TARGETDIR</span></span>                     |
| <span data-ttu-id="c5938-155">Dir1</span><span class="sxs-lookup"><span data-stu-id="c5938-155">Dir1</span></span>      | <span data-ttu-id="c5938-156">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="c5938-156">SOURCEDIR</span></span>         | <span data-ttu-id="c5938-157">Producto \| Component1 del producto:.</span><span class="sxs-lookup"><span data-stu-id="c5938-157">Product\|Component1 Product:.</span></span> |
| <span data-ttu-id="c5938-158">Dir2</span><span class="sxs-lookup"><span data-stu-id="c5938-158">Dir2</span></span>      | <span data-ttu-id="c5938-159">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="c5938-159">SOURCEDIR</span></span>         | <span data-ttu-id="c5938-160">Producto:.</span><span class="sxs-lookup"><span data-stu-id="c5938-160">Product:.</span></span>                     |
| <span data-ttu-id="c5938-161">Dir3</span><span class="sxs-lookup"><span data-stu-id="c5938-161">Dir3</span></span>      | <span data-ttu-id="c5938-162">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="c5938-162">SOURCEDIR</span></span>         | <span data-ttu-id="c5938-163">\|Herramientas comunes comunes:</span><span class="sxs-lookup"><span data-stu-id="c5938-163">Common\|Common Tools:</span></span>         |



 

<span data-ttu-id="c5938-164">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c5938-164">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="c5938-165">Archivo</span><span class="sxs-lookup"><span data-stu-id="c5938-165">File</span></span>  | <span data-ttu-id="c5938-166">Componente\_</span><span class="sxs-lookup"><span data-stu-id="c5938-166">Component\_</span></span> | <span data-ttu-id="c5938-167">FileName</span><span class="sxs-lookup"><span data-stu-id="c5938-167">FileName</span></span>   |
|-------|-------------|------------|
| <span data-ttu-id="c5938-168">Archivo1</span><span class="sxs-lookup"><span data-stu-id="c5938-168">File1</span></span> | <span data-ttu-id="c5938-169">Component1</span><span class="sxs-lookup"><span data-stu-id="c5938-169">Component1</span></span>  | <span data-ttu-id="c5938-170">Léame. 1</span><span class="sxs-lookup"><span data-stu-id="c5938-170">README.1st</span></span> |
| <span data-ttu-id="c5938-171">Archivo2</span><span class="sxs-lookup"><span data-stu-id="c5938-171">File2</span></span> | <span data-ttu-id="c5938-172">Component2</span><span class="sxs-lookup"><span data-stu-id="c5938-172">Component2</span></span>  | <span data-ttu-id="c5938-173">Léame. 1</span><span class="sxs-lookup"><span data-stu-id="c5938-173">README.1st</span></span> |
| <span data-ttu-id="c5938-174">File3</span><span class="sxs-lookup"><span data-stu-id="c5938-174">File3</span></span> | <span data-ttu-id="c5938-175">Component3</span><span class="sxs-lookup"><span data-stu-id="c5938-175">Component3</span></span>  | <span data-ttu-id="c5938-176">Léame. 1</span><span class="sxs-lookup"><span data-stu-id="c5938-176">README.1st</span></span> |
| <span data-ttu-id="c5938-177">File4</span><span class="sxs-lookup"><span data-stu-id="c5938-177">File4</span></span> | <span data-ttu-id="c5938-178">Component4</span><span class="sxs-lookup"><span data-stu-id="c5938-178">Component4</span></span>  | <span data-ttu-id="c5938-179">Léame. 1</span><span class="sxs-lookup"><span data-stu-id="c5938-179">README.1st</span></span> |
| <span data-ttu-id="c5938-180">File5</span><span class="sxs-lookup"><span data-stu-id="c5938-180">File5</span></span> | <span data-ttu-id="c5938-181">Component5</span><span class="sxs-lookup"><span data-stu-id="c5938-181">Component5</span></span>  | <span data-ttu-id="c5938-182">Léame. 1</span><span class="sxs-lookup"><span data-stu-id="c5938-182">README.1st</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c5938-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c5938-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5938-184">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="c5938-184">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




