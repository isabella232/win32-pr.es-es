---
description: Las instancias de ScoredProperty también se pueden anidar dentro de otras instancias de ScoredProperty o como elementos secundarios de una instancia de Option.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Instancias scoredProperty anidadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a80d291fa59b2f36191f42b2f99ea9d22789a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408608"
---
# <a name="nested-scoredproperty-instances"></a><span data-ttu-id="75778-103">Instancias scoredProperty anidadas</span><span class="sxs-lookup"><span data-stu-id="75778-103">Nested ScoredProperty Instances</span></span>

<span data-ttu-id="75778-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="75778-104">This topic is not current.</span></span> <span data-ttu-id="75778-105">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="75778-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="75778-106">Tenga en cuenta que no está restringido a agregar instancias de ScoredProperty como elementos secundarios de una instancia de Option.</span><span class="sxs-lookup"><span data-stu-id="75778-106">Notice that you are not restricted to adding ScoredProperty instances as child elements of an Option instance.</span></span> <span data-ttu-id="75778-107">Las instancias de ScoredProperty también se pueden anidar dentro de otras instancias de ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="75778-107">ScoredProperty instances may also be nested within other ScoredProperty instances.</span></span> <span data-ttu-id="75778-108">Esto resulta útil cuando una propiedad de dispositivo es compleja y se representa mejor mediante varias subpropiedades.</span><span class="sxs-lookup"><span data-stu-id="75778-108">This is useful when a device property is complex and is best represented by multiple subproperties.</span></span> <span data-ttu-id="75778-109">Agregar subpropiedades a una propiedad existente (o pública) o ScoredProperty es una buena manera de mejorar una opción, al tiempo que se conserva la portabilidad con las instancias de option existentes.</span><span class="sxs-lookup"><span data-stu-id="75778-109">Adding subproperties to an existing (or public) Property or ScoredProperty is a good way to enhance an Option, while retaining portability with existing Option instances.</span></span> <span data-ttu-id="75778-110">Por ejemplo, las instancias de opción estándar para la característica MediaType contienen una propiedad ScoredProperty que describe el peso del medio como Light, Medium, Heavy o ExtraHeavy.</span><span class="sxs-lookup"><span data-stu-id="75778-110">For example, the standard Option instances for the MediaType Feature contain a ScoredProperty describing the weight of the media as Light, Medium, Heavy, or ExtraHeavy.</span></span> <span data-ttu-id="75778-111">Si desea descripciones más precisas del peso, puede agregar una subpropiedad (GramsPer100Sheets en el ejemplo siguiente) que contenga el peso real (en gramas) de 100 hojas de medios.</span><span class="sxs-lookup"><span data-stu-id="75778-111">If you want more precise descriptions of the weight, you can add a subproperty (GramsPer100Sheets in the following example) that contains the actual weight (in grams) of 100 sheets of media.</span></span> <span data-ttu-id="75778-112">La opción mejorada podría ser como la del ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="75778-112">The enhanced Option might look like the following example.</span></span>

``` syntax
<!-- Note: The following ScoredProperty is not a Public Print Schema ScoredProperty -->
<!-- This example shows a nested ScoredProperty defined by a Private namespace-->
<!-- It is included for illustration purposes. -->

<psf:ScoredProperty name="FabrikamES500:PaperWeight">
  <psf:Value xsi:type="xs:string">Medium</psf:Value>
  <psf:ScoredProperty name="FabrikamES500:GramsPerSheet">
    <Value xsi:type="decimal">109.5</Value>
  </psf:ScoredProperty>
</psf:ScoredProperty>
```

<span data-ttu-id="75778-113">Una comparación de las instancias de opción original y mejorada genera una coincidencia casi perfecta, porque la opción mejorada es un superconjunto del original y se conservan las ubicaciones y los valores de cada una de las instancias de ScoredProperty originales.</span><span class="sxs-lookup"><span data-stu-id="75778-113">A comparison of the original and enhanced Option instances produces a near-perfect match, because the enhanced Option is a superset of the original, and the locations and values of each of the original ScoredProperty instances is preserved.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75778-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75778-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75778-115">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="75778-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



