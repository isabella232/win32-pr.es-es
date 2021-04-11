---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Definiciones de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5a71bfc5a5111a826b5d221ff1436ecf921dd2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279873"
---
# <a name="parameter-definitions"></a><span data-ttu-id="213ff-104">Definiciones de parámetros</span><span class="sxs-lookup"><span data-stu-id="213ff-104">Parameter Definitions</span></span>

<span data-ttu-id="213ff-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="213ff-105">This topic is not current.</span></span> <span data-ttu-id="213ff-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="213ff-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="213ff-107">En esta sección se describen las definiciones de parámetros públicos que pueden aparecer en un documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="213ff-107">This section outlines the public parameter definitions which may appear in either a PrintCapabilities document.</span></span>

<span data-ttu-id="213ff-108">Los parámetros se usan para describir un intervalo de valores aceptable, en lugar de una enumeración discreta de valores.</span><span class="sxs-lookup"><span data-stu-id="213ff-108">Parameters are used to describe an acceptable range of values, rather than a discrete enumeration of values.</span></span>

## <a name="parameterdef"></a><span data-ttu-id="213ff-109">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="213ff-109">ParameterDef</span></span>

<span data-ttu-id="213ff-110">Para obtener un resumen del tipo de elemento ParameterDef, consulte la sección [ParameterDef](parameterdef.md) .</span><span class="sxs-lookup"><span data-stu-id="213ff-110">For a summary of the ParameterDef element type, please refer to [ParameterDef](parameterdef.md) section.</span></span>

<span data-ttu-id="213ff-111">Para obtener más información sobre la interacción entre los elementos ParameterDef y ParameterInit, consulte la sección [elementos ParameterDef y ParameterInit](./parameterdef-and-parameterinit-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="213ff-111">For more information on the interaction between ParameterDef elements and ParameterInit elements, refer to [ParameterDef and ParameterInit Elements](./parameterdef-and-parameterinit-elements.md) section.</span></span>

<span data-ttu-id="213ff-112">Los elementos ParameterDef que se definen en las palabras clave del esquema de impresión deben estar totalmente definidos en un documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="213ff-112">ParameterDef elements that are defined in the Print Schema Keywords must be fully defined in a PrintCapabilities document.</span></span>

## <a name="parameterref"></a><span data-ttu-id="213ff-113">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="213ff-113">ParameterRef</span></span>

<span data-ttu-id="213ff-114">Para obtener un resumen del tipo de elemento ParameterRef, consulte la sección [ParameterRef](parameterref.md) .</span><span class="sxs-lookup"><span data-stu-id="213ff-114">For a summary of the ParameterRef element type, please refer to [ParameterRef](parameterref.md) section.</span></span>

<span data-ttu-id="213ff-115">Una palabra clave de elemento configurable por el usuario puede contener una referencia a un parámetro.</span><span class="sxs-lookup"><span data-stu-id="213ff-115">A user configurable element keyword may contain a reference to a Parameter.</span></span> <span data-ttu-id="213ff-116">Los elementos ParameterRef se especifican como un elemento secundario de un elemento ScoredProperty para obtener más información, consulte la sección [elementos de referencia de parámetros](parameter-reference-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="213ff-116">ParameterRef elements are specified as a child of a ScoredProperty element For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="213ff-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="213ff-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="213ff-118">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="213ff-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
