---
description: ICEM05 comprueba que el módulo de combinación está asociado correctamente a los componentes del módulo. La asociación incorrecta de un componente con un módulo hace que el componente se asocie incorrectamente a la base de datos de destino.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082538"
---
# <a name="icem05"></a><span data-ttu-id="245da-104">ICEM05</span><span class="sxs-lookup"><span data-stu-id="245da-104">ICEM05</span></span>

<span data-ttu-id="245da-105">ICEM05 comprueba que el módulo de combinación está asociado correctamente a los componentes del módulo.</span><span class="sxs-lookup"><span data-stu-id="245da-105">ICEM05 verifies that the merge module is correctly associated with components in the module.</span></span> <span data-ttu-id="245da-106">La asociación incorrecta de un componente con un módulo hace que el componente se asocie incorrectamente a la base de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="245da-106">Incorrectly associating a component with a module causes the component to be incorrectly associated with the target database.</span></span>

<span data-ttu-id="245da-107">El módulo de combinación ICEs se almacena en un archivo. Cub de módulo de combinación denominado Mergemod. Cub y no en el archivo. Cub que contiene el ICEs usado para la validación del paquete.</span><span class="sxs-lookup"><span data-stu-id="245da-107">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="245da-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="245da-108">Result</span></span>

<span data-ttu-id="245da-109">ICEM05 publica un error si la base de datos del módulo asocia incorrectamente los componentes y el módulo.</span><span class="sxs-lookup"><span data-stu-id="245da-109">ICEM05 posts an error if the module database incorrectly associates components and the module.</span></span>

## <a name="example"></a><span data-ttu-id="245da-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="245da-110">Example</span></span>

<span data-ttu-id="245da-111">ICEM05 expone los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="245da-111">ICEM05 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[<span data-ttu-id="245da-112">ModuleSignature (tabla)</span><span class="sxs-lookup"><span data-stu-id="245da-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="245da-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="245da-113">ModuleID</span></span>         | <span data-ttu-id="245da-114">Idioma</span><span class="sxs-lookup"><span data-stu-id="245da-114">Language</span></span> | <span data-ttu-id="245da-115">Versión</span><span class="sxs-lookup"><span data-stu-id="245da-115">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="245da-116">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="245da-116">MyModule.*GUID1*</span></span> | <span data-ttu-id="245da-117">3082</span><span class="sxs-lookup"><span data-stu-id="245da-117">1033</span></span>     | <span data-ttu-id="245da-118">1,0</span><span class="sxs-lookup"><span data-stu-id="245da-118">1.0</span></span>     |



 

[<span data-ttu-id="245da-119">**Tabla ModuleComponents**</span><span class="sxs-lookup"><span data-stu-id="245da-119">**ModuleComponents Table**</span></span>](modulecomponents-table.md)



| <span data-ttu-id="245da-120">Componente</span><span class="sxs-lookup"><span data-stu-id="245da-120">Component</span></span>  | <span data-ttu-id="245da-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="245da-121">ModuleID</span></span>            | <span data-ttu-id="245da-122">Idioma</span><span class="sxs-lookup"><span data-stu-id="245da-122">Language</span></span> |
|------------|---------------------|----------|
| <span data-ttu-id="245da-123">Component1</span><span class="sxs-lookup"><span data-stu-id="245da-123">Component1</span></span> | <span data-ttu-id="245da-124">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="245da-124">MyModule.*GUID1*</span></span>    | <span data-ttu-id="245da-125">3082</span><span class="sxs-lookup"><span data-stu-id="245da-125">1033</span></span>     |
| <span data-ttu-id="245da-126">Component2</span><span class="sxs-lookup"><span data-stu-id="245da-126">Component2</span></span> | <span data-ttu-id="245da-127">OtherModule. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="245da-127">OtherModule.*GUID2*</span></span> | <span data-ttu-id="245da-128">3082</span><span class="sxs-lookup"><span data-stu-id="245da-128">1033</span></span>     |



 

<span data-ttu-id="245da-129">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="245da-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="245da-130">Componente</span><span class="sxs-lookup"><span data-stu-id="245da-130">Component</span></span>  | <span data-ttu-id="245da-131">ComponentID</span><span class="sxs-lookup"><span data-stu-id="245da-131">ComponentID</span></span> |
|------------|-------------|
| <span data-ttu-id="245da-132">Component3</span><span class="sxs-lookup"><span data-stu-id="245da-132">Component3</span></span> | <span data-ttu-id="245da-133">*GUID4*</span><span class="sxs-lookup"><span data-stu-id="245da-133">*GUID4*</span></span>     |
| <span data-ttu-id="245da-134">Component2</span><span class="sxs-lookup"><span data-stu-id="245da-134">Component2</span></span> | <span data-ttu-id="245da-135">*GUID5*</span><span class="sxs-lookup"><span data-stu-id="245da-135">*GUID5*</span></span>     |



 

<span data-ttu-id="245da-136">El módulo de combinación ICE informa del primer error porque la tabla ModuleComponents intenta asociar un componente a otro módulo que no es el módulo actual especificado en la tabla ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="245da-136">The merge module ICE reports the first error because the ModuleComponents table attempts to associate a component with another module that is not the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="245da-137">Para corregir esto, cambie las columnas ModuleID y Language del registro ModuleComponents de Component2 por el correspondiente al módulo actual, MyModule. *GUID1*.</span><span class="sxs-lookup"><span data-stu-id="245da-137">To fix this, change the ModuleID and Language columns of the ModuleComponents record for Component2 to that for the current module, MyModule.*GUID1*.</span></span>

<span data-ttu-id="245da-138">El módulo de combinación ICE informa del segundo error porque el primer registro de la tabla ModuleComponents intenta asociar Component1 con el módulo.</span><span class="sxs-lookup"><span data-stu-id="245da-138">The merge module ICE reports the second error because the first record in the ModuleComponents table attempts to associate Component1 with the module.</span></span> <span data-ttu-id="245da-139">Este componente no existe en la tabla de componentes del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="245da-139">This component does not exist in the Component Table of the merge module.</span></span> <span data-ttu-id="245da-140">Un módulo solo se puede asociar a un componente que existe en el módulo.</span><span class="sxs-lookup"><span data-stu-id="245da-140">A module can only be associated with a component that exists in the module.</span></span> <span data-ttu-id="245da-141">Para solucionarlo, quite el registro del componente que no existe.</span><span class="sxs-lookup"><span data-stu-id="245da-141">To fix this, remove the record for the non-existent component.</span></span>

<span data-ttu-id="245da-142">El módulo de combinación ICE informa del tercer error porque el módulo intenta agregar Component3 a la base de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="245da-142">The merge module ICE reports the third error because the module attempts to add Component3 to the target database.</span></span> <span data-ttu-id="245da-143">Este componente no se ha asociado al módulo en la tabla ModuleComponents.</span><span class="sxs-lookup"><span data-stu-id="245da-143">This component has not been associated with the module in the ModuleComponents table.</span></span> <span data-ttu-id="245da-144">Para corregir este error, agregue un registro para Component3 a la tabla ModuleComponents.</span><span class="sxs-lookup"><span data-stu-id="245da-144">To fix this error, add a record for Component3 to the ModuleComponents table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="245da-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="245da-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="245da-146">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="245da-146">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



