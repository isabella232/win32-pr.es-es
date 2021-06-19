---
description: Obtenga información sobre las definiciones de parámetros en un documento PrintCapabilities. Este tema no está actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Definiciones de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc8ad2bed3a972202bc0a5bb07cbdd4ef9d8f44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396580"
---
# <a name="parameter-definitions"></a><span data-ttu-id="f603f-105">Definiciones de parámetros</span><span class="sxs-lookup"><span data-stu-id="f603f-105">Parameter Definitions</span></span>

<span data-ttu-id="f603f-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="f603f-106">This topic is not current.</span></span> <span data-ttu-id="f603f-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f603f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f603f-108">En esta sección se describen las definiciones de parámetros públicos que pueden aparecer en un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f603f-108">This section outlines the public parameter definitions which may appear in either a PrintCapabilities document.</span></span>

<span data-ttu-id="f603f-109">Los parámetros se usan para describir un intervalo aceptable de valores, en lugar de una enumeración discreta de valores.</span><span class="sxs-lookup"><span data-stu-id="f603f-109">Parameters are used to describe an acceptable range of values, rather than a discrete enumeration of values.</span></span>

## <a name="parameterdef"></a><span data-ttu-id="f603f-110">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f603f-110">ParameterDef</span></span>

<span data-ttu-id="f603f-111">Para obtener un resumen del tipo de elemento ParameterDef, consulte la [sección ParameterDef.](parameterdef.md)</span><span class="sxs-lookup"><span data-stu-id="f603f-111">For a summary of the ParameterDef element type, please refer to [ParameterDef](parameterdef.md) section.</span></span>

<span data-ttu-id="f603f-112">Para obtener más información sobre la interacción entre los elementos ParameterDef y los elementos ParameterInit, consulte la sección [ParameterDef y ParameterInit Elements.](./parameterdef-and-parameterinit-elements.md)</span><span class="sxs-lookup"><span data-stu-id="f603f-112">For more information on the interaction between ParameterDef elements and ParameterInit elements, refer to [ParameterDef and ParameterInit Elements](./parameterdef-and-parameterinit-elements.md) section.</span></span>

<span data-ttu-id="f603f-113">Los elementos ParameterDef que se definen en las palabras clave de esquema de impresión deben estar totalmente definidos en un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f603f-113">ParameterDef elements that are defined in the Print Schema Keywords must be fully defined in a PrintCapabilities document.</span></span>

## <a name="parameterref"></a><span data-ttu-id="f603f-114">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="f603f-114">ParameterRef</span></span>

<span data-ttu-id="f603f-115">Para obtener un resumen del tipo de elemento ParameterRef, consulte la [sección ParameterRef.](parameterref.md)</span><span class="sxs-lookup"><span data-stu-id="f603f-115">For a summary of the ParameterRef element type, please refer to [ParameterRef](parameterref.md) section.</span></span>

<span data-ttu-id="f603f-116">Una palabra clave de elemento configurable por el usuario puede contener una referencia a un parámetro .</span><span class="sxs-lookup"><span data-stu-id="f603f-116">A user configurable element keyword may contain a reference to a Parameter.</span></span> <span data-ttu-id="f603f-117">Los elementos ParameterRef se especifican como elementos secundarios de un elemento ScoredProperty. Para más información, consulte la sección [Elementos de referencia de](parameter-reference-elements.md) parámetros.</span><span class="sxs-lookup"><span data-stu-id="f603f-117">ParameterRef elements are specified as a child of a ScoredProperty element For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f603f-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f603f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f603f-119">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="f603f-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
