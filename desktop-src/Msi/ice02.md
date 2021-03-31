---
description: ICE02 valida que ciertas referencias entre el componente, el archivo y las tablas del registro sean recíprocas. Estas referencias deben ser recíprocas para que el instalador determine correctamente el estado de instalación de los componentes.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808750"
---
# <a name="ice02"></a><span data-ttu-id="b918e-104">ICE02</span><span class="sxs-lookup"><span data-stu-id="b918e-104">ICE02</span></span>

<span data-ttu-id="b918e-105">ICE02 valida que ciertas referencias entre el [componente](component-table.md), el [archivo](file-table.md)y las tablas [del registro](registry-table.md) sean recíprocas.</span><span class="sxs-lookup"><span data-stu-id="b918e-105">ICE02 validates that certain references between the [Component](component-table.md), [File](file-table.md), and [Registry](registry-table.md) tables are reciprocal.</span></span> <span data-ttu-id="b918e-106">Estas referencias deben ser recíprocas para que el instalador determine correctamente el estado de instalación de los componentes.</span><span class="sxs-lookup"><span data-stu-id="b918e-106">These references must to be reciprocal for the installer to correctly determine the installation state of components.</span></span>

<span data-ttu-id="b918e-107">El instalador usa la columna de ruta de la tabla de componentes para detectar la presencia del componente que aparece en la columna componente.</span><span class="sxs-lookup"><span data-stu-id="b918e-107">The installer uses the KeyPath column of the Component table to detect the presence of the component listed in the Component column.</span></span> <span data-ttu-id="b918e-108">La columna de ruta de acceso contiene una clave en las tablas del registro o del archivo.</span><span class="sxs-lookup"><span data-stu-id="b918e-108">The KeyPath column contains a key into the Registry or File tables.</span></span> <span data-ttu-id="b918e-109">Ambas tablas tienen una \_ columna componente que contiene una clave de nuevo en la tabla componente que apunta al componente que controla la entrada o el archivo del registro.</span><span class="sxs-lookup"><span data-stu-id="b918e-109">Both of these tables have a Component\_ column that contains a key back into the Component table pointing to the component that controls the registry entry or file.</span></span> <span data-ttu-id="b918e-110">Estas referencias deben ser recíprocas.</span><span class="sxs-lookup"><span data-stu-id="b918e-110">These references must be reciprocal.</span></span>

## <a name="result"></a><span data-ttu-id="b918e-111">Resultado</span><span class="sxs-lookup"><span data-stu-id="b918e-111">Result</span></span>

<span data-ttu-id="b918e-112">ICE02 envía un mensaje de error si encuentra una referencia que debe ser recíproca y no es.</span><span class="sxs-lookup"><span data-stu-id="b918e-112">ICE02 posts an error message if it finds a reference that should be reciprocal and is not.</span></span>

## <a name="example"></a><span data-ttu-id="b918e-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b918e-113">Example</span></span>

<span data-ttu-id="b918e-114">ICE02 publicaría el siguiente mensaje de error para un archivo. msi que contiene las entradas de base de datos que se muestran.</span><span class="sxs-lookup"><span data-stu-id="b918e-114">ICE02 would post the following error message for a .msi file containing the database entries shown.</span></span>

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

<span data-ttu-id="b918e-115">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="b918e-115">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="b918e-116">Componente</span><span class="sxs-lookup"><span data-stu-id="b918e-116">Component</span></span> | <span data-ttu-id="b918e-117">Rutas</span><span class="sxs-lookup"><span data-stu-id="b918e-117">KeyPath</span></span>   |
|-----------|-----------|
| <span data-ttu-id="b918e-118">Rojo</span><span class="sxs-lookup"><span data-stu-id="b918e-118">Red</span></span>       | <span data-ttu-id="b918e-119">\_Archivo rojo</span><span class="sxs-lookup"><span data-stu-id="b918e-119">Red\_File</span></span> |
| <span data-ttu-id="b918e-120">Azul</span><span class="sxs-lookup"><span data-stu-id="b918e-120">Blue</span></span>      | <span data-ttu-id="b918e-121">\_Archivo rojo</span><span class="sxs-lookup"><span data-stu-id="b918e-121">Red\_File</span></span> |



 

<span data-ttu-id="b918e-122">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="b918e-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="b918e-123">Columna de archivo</span><span class="sxs-lookup"><span data-stu-id="b918e-123">File Column</span></span> | <span data-ttu-id="b918e-124">Componente\_</span><span class="sxs-lookup"><span data-stu-id="b918e-124">Component\_</span></span> |
|-------------|-------------|
| <span data-ttu-id="b918e-125">\_Archivo rojo</span><span class="sxs-lookup"><span data-stu-id="b918e-125">Red\_File</span></span>   | <span data-ttu-id="b918e-126">Rojo</span><span class="sxs-lookup"><span data-stu-id="b918e-126">Red</span></span>         |
| <span data-ttu-id="b918e-127">\_Archivo azul</span><span class="sxs-lookup"><span data-stu-id="b918e-127">Blue\_File</span></span>  | <span data-ttu-id="b918e-128">Azul</span><span class="sxs-lookup"><span data-stu-id="b918e-128">Blue</span></span>        |



 

<span data-ttu-id="b918e-129">El componente azul hace referencia \_ al archivo rojo, pero \_ el archivo rojo no está controlado por el componente azul y, por lo tanto, no puede ser el archivo de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="b918e-129">Component Blue references Red\_File, but Red\_File is not controlled by Component Blue and therefore cannot be the KeyPath file.</span></span> <span data-ttu-id="b918e-130">Si se llamó al instalador para obtener el estado de instalación azul, comprobará incorrectamente si \_ se instaló el archivo rojo.</span><span class="sxs-lookup"><span data-stu-id="b918e-130">If the installer were called to get the installation state of Blue it would incorrectly check whether Red\_File was installed.</span></span> <span data-ttu-id="b918e-131">Si cambia el campo de ruta de la ruta de acceso azul en la tabla de componentes al archivo azul, se \_ corregirá el error.</span><span class="sxs-lookup"><span data-stu-id="b918e-131">Changing the KeyPath field for Blue in the Component Table to Blue\_File fixes the error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b918e-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b918e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b918e-133">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="b918e-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



