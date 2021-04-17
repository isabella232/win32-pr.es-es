---
description: ICEM10 comprueba que un módulo de combinación solo contiene las propiedades que se permiten en la tabla de propiedades.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652860"
---
# <a name="icem10"></a><span data-ttu-id="7cfd3-103">ICEM10</span><span class="sxs-lookup"><span data-stu-id="7cfd3-103">ICEM10</span></span>

<span data-ttu-id="7cfd3-104">ICEM10 comprueba que un módulo de combinación solo contiene las propiedades que se permiten en la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="7cfd3-104">ICEM10 verifies that a merge module contains only properties that are allowed in the [Property Table](property-table.md).</span></span> <span data-ttu-id="7cfd3-105">No se permiten las siguientes propiedades específicas del producto en la tabla de propiedades:</span><span class="sxs-lookup"><span data-stu-id="7cfd3-105">The following product specific properties are not allowed in the Property Table:</span></span>

-   [<span data-ttu-id="7cfd3-106">**Propiedad ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="7cfd3-106">**ProductLanguage Property**</span></span>](productlanguage.md)
-   [<span data-ttu-id="7cfd3-107">**Propiedad ProductCode**</span><span class="sxs-lookup"><span data-stu-id="7cfd3-107">**ProductCode Property**</span></span>](productcode.md)
-   [<span data-ttu-id="7cfd3-108">**Propiedad ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="7cfd3-108">**ProductVersion Property**</span></span>](productversion.md)
-   [<span data-ttu-id="7cfd3-109">**ProductName (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="7cfd3-109">**ProductName Property**</span></span>](productname.md)
-   [<span data-ttu-id="7cfd3-110">**Propiedad manufacturer**</span><span class="sxs-lookup"><span data-stu-id="7cfd3-110">**Manufacturer Property**</span></span>](manufacturer.md)

## <a name="result"></a><span data-ttu-id="7cfd3-111">Resultado</span><span class="sxs-lookup"><span data-stu-id="7cfd3-111">Result</span></span>

<span data-ttu-id="7cfd3-112">ICEM10 expone un error cuando un módulo de combinación contiene una propiedad que no está permitida en la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="7cfd3-112">ICEM10 posts an error when a merge module contains a property that is not allowed in the [Property Table](property-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="7cfd3-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7cfd3-113">Example</span></span>

<span data-ttu-id="7cfd3-114">ICEM10 expone los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran.</span><span class="sxs-lookup"><span data-stu-id="7cfd3-114">ICEM10 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

<span data-ttu-id="7cfd3-115">En la tabla siguiente se muestra una [tabla de propiedades](property-table.md)parciales.</span><span class="sxs-lookup"><span data-stu-id="7cfd3-115">The following table shows you a partial [Property Table](property-table.md).</span></span>



| <span data-ttu-id="7cfd3-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7cfd3-116">Property</span></span>                                   | <span data-ttu-id="7cfd3-117">Valores</span><span class="sxs-lookup"><span data-stu-id="7cfd3-117">Values</span></span>    |
|--------------------------------------------|-----------|
| <span data-ttu-id="7cfd3-118">Color</span><span class="sxs-lookup"><span data-stu-id="7cfd3-118">Color</span></span>                                      | <span data-ttu-id="7cfd3-119">Rojo</span><span class="sxs-lookup"><span data-stu-id="7cfd3-119">Red</span></span>       |
| [<span data-ttu-id="7cfd3-120">**Le**</span><span class="sxs-lookup"><span data-stu-id="7cfd3-120">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="7cfd3-121">Microsoft</span><span class="sxs-lookup"><span data-stu-id="7cfd3-121">Microsoft</span></span> |
| [<span data-ttu-id="7cfd3-122">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="7cfd3-122">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="7cfd3-123">3082</span><span class="sxs-lookup"><span data-stu-id="7cfd3-123">1033</span></span>      |



 

<span data-ttu-id="7cfd3-124">En el procedimiento siguiente se muestra cómo corregir los errores.</span><span class="sxs-lookup"><span data-stu-id="7cfd3-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="7cfd3-125">**Para corregir los errores**</span><span class="sxs-lookup"><span data-stu-id="7cfd3-125">**To fix the errors**</span></span>

1.  <span data-ttu-id="7cfd3-126">Quite la propiedad '[**manufacturer**](manufacturer.md)' de la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="7cfd3-126">Remove the '[**Manufacturer**](manufacturer.md)' property from the [Property Table](property-table.md).</span></span>
2.  <span data-ttu-id="7cfd3-127">Quite la propiedad '[**ProductLanguage**](productlanguage.md)' de la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="7cfd3-127">Remove the '[**ProductLanguage**](productlanguage.md)' property from the [Property Table](property-table.md).</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="7cfd3-128">Tabla utilizada durante la ejecución</span><span class="sxs-lookup"><span data-stu-id="7cfd3-128">Table Used During Execution</span></span>

<span data-ttu-id="7cfd3-129">La [tabla de propiedades](property-table.md) se usa durante la ejecución.</span><span class="sxs-lookup"><span data-stu-id="7cfd3-129">The [Property Table](property-table.md) is used during execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cfd3-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7cfd3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cfd3-131">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="7cfd3-131">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



