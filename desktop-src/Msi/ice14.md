---
description: ICE14 valida la tabla de características de una base de datos Windows Installer.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360864"
---
# <a name="ice14"></a><span data-ttu-id="2354e-103">ICE14</span><span class="sxs-lookup"><span data-stu-id="2354e-103">ICE14</span></span>

<span data-ttu-id="2354e-104">ICE14 valida las características siguientes:</span><span class="sxs-lookup"><span data-stu-id="2354e-104">ICE14 validates the following for features:</span></span>

-   <span data-ttu-id="2354e-105">Dichas características principales de raíz no tienen el bit msidbFeatureAttributesFollowParent establecido en la columna Attributes de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="2354e-105">That root parent features do not have the msidbFeatureAttributesFollowParent bit set in the Attributes column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="2354e-106">Una característica raíz no tiene un elemento primario.</span><span class="sxs-lookup"><span data-stu-id="2354e-106">A root feature does not have a parent.</span></span>
-   <span data-ttu-id="2354e-107">No hay ninguna característica que tenga la misma entrada en las \_ columnas primarias de características y características de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="2354e-107">That no feature has the same entry in the Feature and Feature\_Parent columns of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="2354e-108">Ninguna característica puede ser su propio elemento primario.</span><span class="sxs-lookup"><span data-stu-id="2354e-108">No feature can be its own parent.</span></span>

## <a name="result"></a><span data-ttu-id="2354e-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="2354e-109">Result</span></span>

<span data-ttu-id="2354e-110">ICE14 envía un mensaje de error si encuentra una característica raíz con el conjunto de bits msidbFeatureAttributesFollowParent o una característica con entradas idénticas en las \_ columnas primarias de características y características de la tabla de características.</span><span class="sxs-lookup"><span data-stu-id="2354e-110">ICE14 posts an error message if it finds a root feature with the msidbFeatureAttributesFollowParent bit set or a feature with identical entries in the Feature and Feature\_Parent columns of the Feature table.</span></span>

## <a name="example"></a><span data-ttu-id="2354e-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2354e-111">Example</span></span>

<span data-ttu-id="2354e-112">ICE14 devolverá los siguientes errores en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2354e-112">ICE14 would return the following errors for the following example:</span></span>

-   <span data-ttu-id="2354e-113">La característica deporte tiene el mismo valor en las columnas principales característica y característica \_ de la tabla archivo.</span><span class="sxs-lookup"><span data-stu-id="2354e-113">The feature Sport has the same value in the Feature and Feature\_Parent columns of the File table.</span></span>
-   <span data-ttu-id="2354e-114">El deporte de la característica raíz tiene establecido el bit msidbFeatureAttributesFollowParent.</span><span class="sxs-lookup"><span data-stu-id="2354e-114">The root feature Sport has the msidbFeatureAttributesFollowParent bit set.</span></span>

<span data-ttu-id="2354e-115">En el árbol de características de este ejemplo, deporte es la característica raíz y una principal de las características de natación y fútbol.</span><span class="sxs-lookup"><span data-stu-id="2354e-115">In the feature tree of this example, Sport is the root feature and a parent of the Swimming and Football features.</span></span> <span data-ttu-id="2354e-116">Freestyle es una característica secundaria de natación.</span><span class="sxs-lookup"><span data-stu-id="2354e-116">Freestyle is a child feature of Swimming.</span></span> <span data-ttu-id="2354e-117">TouchFootball es una característica secundaria de fútbol.</span><span class="sxs-lookup"><span data-stu-id="2354e-117">TouchFootball is a child feature of Football.</span></span>

<span data-ttu-id="2354e-118">[Tabla de características](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="2354e-118">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="2354e-119">Característica</span><span class="sxs-lookup"><span data-stu-id="2354e-119">Feature</span></span>       | <span data-ttu-id="2354e-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="2354e-120">Attributes</span></span> | <span data-ttu-id="2354e-121">Característica \_ principal</span><span class="sxs-lookup"><span data-stu-id="2354e-121">Feature\_Parent</span></span> |
|---------------|------------|-----------------|
| <span data-ttu-id="2354e-122">Deporte</span><span class="sxs-lookup"><span data-stu-id="2354e-122">Sport</span></span>         | <span data-ttu-id="2354e-123">4</span><span class="sxs-lookup"><span data-stu-id="2354e-123">4</span></span>          | <span data-ttu-id="2354e-124">Deporte</span><span class="sxs-lookup"><span data-stu-id="2354e-124">Sport</span></span>           |
| <span data-ttu-id="2354e-125">Estiliza</span><span class="sxs-lookup"><span data-stu-id="2354e-125">Swimming</span></span>      | <span data-ttu-id="2354e-126">1</span><span class="sxs-lookup"><span data-stu-id="2354e-126">1</span></span>          | <span data-ttu-id="2354e-127">Deporte</span><span class="sxs-lookup"><span data-stu-id="2354e-127">Sport</span></span>           |
| <span data-ttu-id="2354e-128">Balón</span><span class="sxs-lookup"><span data-stu-id="2354e-128">Football</span></span>      | <span data-ttu-id="2354e-129">4</span><span class="sxs-lookup"><span data-stu-id="2354e-129">4</span></span>          | <span data-ttu-id="2354e-130">Deporte</span><span class="sxs-lookup"><span data-stu-id="2354e-130">Sport</span></span>           |
| <span data-ttu-id="2354e-131">Freestyle</span><span class="sxs-lookup"><span data-stu-id="2354e-131">Freestyle</span></span>     | <span data-ttu-id="2354e-132">1</span><span class="sxs-lookup"><span data-stu-id="2354e-132">1</span></span>          | <span data-ttu-id="2354e-133">Estiliza</span><span class="sxs-lookup"><span data-stu-id="2354e-133">Swimming</span></span>        |
| <span data-ttu-id="2354e-134">TouchFootball</span><span class="sxs-lookup"><span data-stu-id="2354e-134">TouchFootball</span></span> | <span data-ttu-id="2354e-135">4</span><span class="sxs-lookup"><span data-stu-id="2354e-135">4</span></span>          | <span data-ttu-id="2354e-136">Balón</span><span class="sxs-lookup"><span data-stu-id="2354e-136">Football</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2354e-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2354e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2354e-138">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="2354e-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



