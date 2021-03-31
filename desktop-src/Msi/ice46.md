---
description: ICE46 comprueba si hay propiedades personalizadas en condiciones, texto con formato y otras ubicaciones que difieren de una propiedad definida por el sistema solo en el caso de uno o más caracteres.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813323"
---
# <a name="ice46"></a><span data-ttu-id="e8f08-103">ICE46</span><span class="sxs-lookup"><span data-stu-id="e8f08-103">ICE46</span></span>

<span data-ttu-id="e8f08-104">ICE46 comprueba si hay propiedades personalizadas en condiciones, texto con formato y otras ubicaciones que difieren de una propiedad definida por el sistema solo en el caso de uno o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="e8f08-104">ICE46 checks for custom properties in conditions, formatted text, and other locations that differ from a system defined property only by the case of one or more characters.</span></span>

## <a name="result"></a><span data-ttu-id="e8f08-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="e8f08-105">Result</span></span>

<span data-ttu-id="e8f08-106">ICE46 envía un mensaje informativo si hay una propiedad personalizada en una condición, texto con formato y otra ubicación que difiere de las propiedades definidas por el sistema solo en el caso de uno o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="e8f08-106">ICE46 posts an informational message if there is a custom property in a condition, formatted text, and other location that differs from a system defined properties only in the case of one or more characters.</span></span>

## <a name="example"></a><span data-ttu-id="e8f08-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8f08-107">Example</span></span>

<span data-ttu-id="e8f08-108">ICE46 notifica los siguientes errores para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="e8f08-108">ICE46 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="e8f08-109">Error ICE46</span><span class="sxs-lookup"><span data-stu-id="e8f08-109">ICE46 error</span></span>                                                                                                                                            | <span data-ttu-id="e8f08-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8f08-110">Description</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f08-111">La propiedad ReinstallMode definida en la tabla de propiedades solo se diferencia de otra propiedad definida por el uso de mayúsculas o minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e8f08-111">Property ReinstallMode defined in property table differs from another defined property only by case.</span></span>                                                   | <span data-ttu-id="e8f08-112">El nombre de propiedad de System Defined **REINSTALLMODE** solo se diferencia de la propiedad personalizada por el uso de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e8f08-112">The system defined property name **REINSTALLMODE** differs from the custom property by case only.</span></span> <span data-ttu-id="e8f08-113">Las propiedades distinguen mayúsculas de minúsculas, por lo que la propiedad personalizada no es igual que la propiedad del sistema.</span><span class="sxs-lookup"><span data-stu-id="e8f08-113">Properties are case sensitive, so custom property is not the same as the system property.</span></span> <span data-ttu-id="e8f08-114">Se trata de una causa común de los errores.</span><span class="sxs-lookup"><span data-stu-id="e8f08-114">This is a common cause of errors.</span></span> |
| <span data-ttu-id="e8f08-115">Se hace referencia a la propiedad ' propiedad ' en la columna ' InstallExecuteSequence '. ' La condición ' de la fila ' InstallFinalize ' es distinta de una propiedad definida por el uso de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e8f08-115">Property 'Myproperty' referenced in column 'InstallExecuteSequence'.'Condition' of row 'InstallFinalize' differs from a defined property by case only.</span></span> | <span data-ttu-id="e8f08-116">La tabla de propiedades define la propiedad de la tabla, pero la propiedad a la que se hace referencia es propiedad.</span><span class="sxs-lookup"><span data-stu-id="e8f08-116">The property table defines the table MyProperty, but the referenced property is Myproperty.</span></span> <span data-ttu-id="e8f08-117">Las propiedades distinguen mayúsculas de minúsculas, por lo que las dos propiedades no son iguales.</span><span class="sxs-lookup"><span data-stu-id="e8f08-117">Properties are case sensitive, so the two properties are NOT the same.</span></span> <span data-ttu-id="e8f08-118">Se trata de una causa común de los errores.</span><span class="sxs-lookup"><span data-stu-id="e8f08-118">This is a common cause of errors.</span></span>                          |



 

[<span data-ttu-id="e8f08-119">Tabla de propiedades</span><span class="sxs-lookup"><span data-stu-id="e8f08-119">Property Table</span></span>](property-table.md)



| <span data-ttu-id="e8f08-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e8f08-120">Property</span></span>      | <span data-ttu-id="e8f08-121">Value</span><span class="sxs-lookup"><span data-stu-id="e8f08-121">Value</span></span>   |
|---------------|---------|
| <span data-ttu-id="e8f08-122">ReinstallMode</span><span class="sxs-lookup"><span data-stu-id="e8f08-122">ReinstallMode</span></span> | <span data-ttu-id="e8f08-123">OMUs</span><span class="sxs-lookup"><span data-stu-id="e8f08-123">omus</span></span>    |
| <span data-ttu-id="e8f08-124">MyProperty</span><span class="sxs-lookup"><span data-stu-id="e8f08-124">MyProperty</span></span>    | <span data-ttu-id="e8f08-125">un valor</span><span class="sxs-lookup"><span data-stu-id="e8f08-125">a value</span></span> |



 

<span data-ttu-id="e8f08-126">[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="e8f08-126">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="e8f08-127">Acción</span><span class="sxs-lookup"><span data-stu-id="e8f08-127">Action</span></span>          | <span data-ttu-id="e8f08-128">Condición</span><span class="sxs-lookup"><span data-stu-id="e8f08-128">Condition</span></span>  |
|-----------------|------------|
| <span data-ttu-id="e8f08-129">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="e8f08-129">InstallFinalize</span></span> | <span data-ttu-id="e8f08-130">MyProperty</span><span class="sxs-lookup"><span data-stu-id="e8f08-130">Myproperty</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e8f08-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8f08-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8f08-132">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="e8f08-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



