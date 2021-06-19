---
description: Obtenga información sobre los elementos ParameterRef en el marco de esquema de impresión. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Elementos ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2935317bc4107e2071911ab1df826426b2bcec17
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396530"
---
# <a name="parameterref-elements"></a><span data-ttu-id="97b5c-105">Elementos ParameterRef</span><span class="sxs-lookup"><span data-stu-id="97b5c-105">ParameterRef Elements</span></span>

<span data-ttu-id="97b5c-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="97b5c-106">This topic is not current.</span></span> <span data-ttu-id="97b5c-107">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="97b5c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="97b5c-108">Los elementos ParameterRef se aplican específicamente a los elementos Option, lo que permite que ese elemento Option haga referencia a un elemento ParameterDef determinado.</span><span class="sxs-lookup"><span data-stu-id="97b5c-108">ParameterRef elements specifically apply to Option elements, allowing the ability for that Option element to refer to a particular ParameterDef element.</span></span> <span data-ttu-id="97b5c-109">Para estos elementos Option, un elemento ScoredProperty que caracteriza a Option no está codificado de forma segura en el documento PrintCapabilities como un valor, sino que es variable.</span><span class="sxs-lookup"><span data-stu-id="97b5c-109">For these Option elements, a ScoredProperty element that characterizes the Option is not hard-coded in the PrintCapabilities document as a Value, but instead is variable.</span></span> <span data-ttu-id="97b5c-110">Para habilitar esta variabilidad, estos elementos ScoredProperty contienen un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="97b5c-110">To enable this variability, these ScoredProperty elements contain a ParameterRef element.</span></span> <span data-ttu-id="97b5c-111">Un elemento ScoredProperty no puede contener un elemento Value ni un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="97b5c-111">A ScoredProperty element may not contain both a Value element and a ParameterRef element.</span></span> <span data-ttu-id="97b5c-112">Los elementos option que contienen uno o varios elementos ParameterRef se denominan elementos Option con parámetros.</span><span class="sxs-lookup"><span data-stu-id="97b5c-112">Option elements containing one or more ParameterRef elements are called parameterized Option elements.</span></span>

<span data-ttu-id="97b5c-113">El marco de esquema de impresión permite que un elemento Option contenga cualquier número de elementos ScoredProperty que hacen referencia a elementos Parameter, junto con cualquier número de elementos ScoredProperty que contengan elementos Value.</span><span class="sxs-lookup"><span data-stu-id="97b5c-113">The Print Schema Framework allows an Option element to contain any number of ScoredProperty elements that refer to Parameter elements, together with any number of ScoredProperty elements that contain Value elements.</span></span> <span data-ttu-id="97b5c-114">El marco también permite que cualquier número de elementos Feature contenga elementos Option con parámetros, y se permite cualquier número de elementos Option con parámetros para cada elemento Feature.</span><span class="sxs-lookup"><span data-stu-id="97b5c-114">The Framework also allows any number of Feature elements to contain parameterized Option elements, and any number of parameterized Option elements are permitted for each Feature element.</span></span> <span data-ttu-id="97b5c-115">Además, se puede hacer referencia a la misma construcción de parámetros mediante varios elementos Option diferentes, elementos Option que pueden pertenecer al mismo elemento Feature o a otro.</span><span class="sxs-lookup"><span data-stu-id="97b5c-115">Also, the same parameter construct can be referred to by several different Option elements, Option elements that can belong to the same or different Feature elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97b5c-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97b5c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97b5c-117">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="97b5c-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



