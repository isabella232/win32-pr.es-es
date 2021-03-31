---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Elementos ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c0e145e99b1ee705d63449cf693c6fc87f6463
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104083602"
---
# <a name="parameterref-elements"></a><span data-ttu-id="613a5-104">Elementos ParameterRef</span><span class="sxs-lookup"><span data-stu-id="613a5-104">ParameterRef Elements</span></span>

<span data-ttu-id="613a5-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="613a5-105">This topic is not current.</span></span> <span data-ttu-id="613a5-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="613a5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="613a5-107">Los elementos ParameterRef se aplican específicamente a los elementos Option, lo que permite que ese elemento OPTION haga referencia a un elemento ParameterDef determinado.</span><span class="sxs-lookup"><span data-stu-id="613a5-107">ParameterRef elements specifically apply to Option elements, allowing the ability for that Option element to refer to a particular ParameterDef element.</span></span> <span data-ttu-id="613a5-108">Para estos elementos Option, un elemento ScoredProperty que caracteriza la opción no está codificado de forma rígida en el documento PrintCapabilities como un valor, sino que es variable.</span><span class="sxs-lookup"><span data-stu-id="613a5-108">For these Option elements, a ScoredProperty element that characterizes the Option is not hard-coded in the PrintCapabilities document as a Value, but instead is variable.</span></span> <span data-ttu-id="613a5-109">Para habilitar esta variabilidad, estos elementos ScoredProperty contienen un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="613a5-109">To enable this variability, these ScoredProperty elements contain a ParameterRef element.</span></span> <span data-ttu-id="613a5-110">Un elemento ScoredProperty no puede contener un elemento Value y un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="613a5-110">A ScoredProperty element may not contain both a Value element and a ParameterRef element.</span></span> <span data-ttu-id="613a5-111">Los elementos de opción que contienen uno o más elementos ParameterRef se denominan elementos de opción parametrizados.</span><span class="sxs-lookup"><span data-stu-id="613a5-111">Option elements containing one or more ParameterRef elements are called parameterized Option elements.</span></span>

<span data-ttu-id="613a5-112">El marco de trabajo de esquema de impresión permite que un elemento OPTION contenga cualquier número de elementos ScoredProperty que hagan referencia a elementos de parámetro, junto con cualquier número de elementos ScoredProperty que contengan elementos de valor.</span><span class="sxs-lookup"><span data-stu-id="613a5-112">The Print Schema Framework allows an Option element to contain any number of ScoredProperty elements that refer to Parameter elements, together with any number of ScoredProperty elements that contain Value elements.</span></span> <span data-ttu-id="613a5-113">El marco de trabajo también permite que cualquier número de elementos de característica contengan elementos de opción parametrizados, y se permite cualquier número de elementos de opción con parámetros para cada elemento de característica.</span><span class="sxs-lookup"><span data-stu-id="613a5-113">The Framework also allows any number of Feature elements to contain parameterized Option elements, and any number of parameterized Option elements are permitted for each Feature element.</span></span> <span data-ttu-id="613a5-114">Además, se puede hacer referencia a la misma construcción de parámetro mediante varios elementos de opción diferentes, elementos de opción que pueden pertenecer a los mismos elementos de característica o a otros distintos.</span><span class="sxs-lookup"><span data-stu-id="613a5-114">Also, the same parameter construct can be referred to by several different Option elements, Option elements that can belong to the same or different Feature elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="613a5-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="613a5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="613a5-116">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="613a5-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



