---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Instancias de ScoredProperty anidadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1bfed09c48bc0ac6e93e09f96dc8116e8b0a91
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689691"
---
# <a name="nested-scoredproperty-instances"></a><span data-ttu-id="92f7d-104">Instancias de ScoredProperty anidadas</span><span class="sxs-lookup"><span data-stu-id="92f7d-104">Nested ScoredProperty Instances</span></span>

<span data-ttu-id="92f7d-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="92f7d-105">This topic is not current.</span></span> <span data-ttu-id="92f7d-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="92f7d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="92f7d-107">Tenga en cuenta que no está restringido a la adición de instancias de ScoredProperty como elementos secundarios de una instancia de opción.</span><span class="sxs-lookup"><span data-stu-id="92f7d-107">Notice that you are not restricted to adding ScoredProperty instances as child elements of an Option instance.</span></span> <span data-ttu-id="92f7d-108">Las instancias de ScoredProperty también se pueden anidar dentro de otras instancias de ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="92f7d-108">ScoredProperty instances may also be nested within other ScoredProperty instances.</span></span> <span data-ttu-id="92f7d-109">Esto resulta útil cuando una propiedad de dispositivo es compleja y se representa mejor mediante varias subpropiedades.</span><span class="sxs-lookup"><span data-stu-id="92f7d-109">This is useful when a device property is complex and is best represented by multiple subproperties.</span></span> <span data-ttu-id="92f7d-110">Agregar subpropiedades a una propiedad (o pública) existente o ScoredProperty es una buena forma de mejorar una opción, a la vez que conserva la portabilidad con las instancias de opción existentes.</span><span class="sxs-lookup"><span data-stu-id="92f7d-110">Adding subproperties to an existing (or public) Property or ScoredProperty is a good way to enhance an Option, while retaining portability with existing Option instances.</span></span> <span data-ttu-id="92f7d-111">Por ejemplo, las instancias de opción estándar de la característica MediaType contienen un ScoredProperty que describe el peso del medio como ligero, medio, pesado o extrapesado.</span><span class="sxs-lookup"><span data-stu-id="92f7d-111">For example, the standard Option instances for the MediaType Feature contain a ScoredProperty describing the weight of the media as Light, Medium, Heavy, or ExtraHeavy.</span></span> <span data-ttu-id="92f7d-112">Si desea obtener descripciones más precisas de la ponderación, puede Agregar una subpropiedad (GramsPer100Sheets en el ejemplo siguiente) que contenga el peso real (en gramos) de 100 hojas de medios.</span><span class="sxs-lookup"><span data-stu-id="92f7d-112">If you want more precise descriptions of the weight, you can add a subproperty (GramsPer100Sheets in the following example) that contains the actual weight (in grams) of 100 sheets of media.</span></span> <span data-ttu-id="92f7d-113">La opción mejorada podría ser similar a la del ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="92f7d-113">The enhanced Option might look like the following example.</span></span>

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

<span data-ttu-id="92f7d-114">Una comparación de las instancias de opciones originales y mejoradas genera una coincidencia casi perfecta, ya que la opción mejorada es un supraconjunto del original, y se conservan las ubicaciones y los valores de cada una de las instancias de ScoredProperty originales.</span><span class="sxs-lookup"><span data-stu-id="92f7d-114">A comparison of the original and enhanced Option instances produces a near-perfect match, because the enhanced Option is a superset of the original, and the locations and values of each of the original ScoredProperty instances is preserved.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92f7d-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92f7d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92f7d-116">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="92f7d-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



