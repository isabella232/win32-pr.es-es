---
description: Contiene una colección de objetos que implementan la interfaz IInkAnalysisRecognizer y que representan la capacidad de reconocer escritura a mano, objetos o gestos.
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: Interfaz IInkAnalysisRecognizers (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360342"
---
# <a name="iinkanalysisrecognizers-interface"></a><span data-ttu-id="6c909-103">Interfaz IInkAnalysisRecognizers</span><span class="sxs-lookup"><span data-stu-id="6c909-103">IInkAnalysisRecognizers interface</span></span>

<span data-ttu-id="6c909-104">Contiene una colección de objetos que implementan la interfaz [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) y que representan la capacidad de reconocer escritura a mano, objetos o gestos.</span><span class="sxs-lookup"><span data-stu-id="6c909-104">Contains a collection of objects that implement the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) interface and that represent the ability to recognize handwriting, objects, or gestures.</span></span>

## <a name="members"></a><span data-ttu-id="6c909-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c909-105">Members</span></span>

<span data-ttu-id="6c909-106">La interfaz **IInkAnalysisRecognizers** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6c909-106">The **IInkAnalysisRecognizers** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6c909-107">**IInkAnalysisRecognizers** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6c909-107">**IInkAnalysisRecognizers** also has these types of members:</span></span>

-   [<span data-ttu-id="6c909-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c909-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6c909-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c909-109">Methods</span></span>

<span data-ttu-id="6c909-110">La interfaz **IInkAnalysisRecognizers** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6c909-110">The **IInkAnalysisRecognizers** interface has these methods.</span></span>



| <span data-ttu-id="6c909-111">Método</span><span class="sxs-lookup"><span data-stu-id="6c909-111">Method</span></span>                                                                               | <span data-ttu-id="6c909-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c909-112">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c909-113">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="6c909-113">**GetCount**</span></span>](iinkanalysisrecognizers-getcount.md)                                 | <span data-ttu-id="6c909-114">Recupera el número de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) de esta colección.</span><span class="sxs-lookup"><span data-stu-id="6c909-114">Retrieves the number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span><br/> |
| [<span data-ttu-id="6c909-115">**GetInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="6c909-115">**GetInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | <span data-ttu-id="6c909-116">Recupera el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="6c909-116">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="6c909-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c909-117">Remarks</span></span>

<span data-ttu-id="6c909-118">El método [**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) de [**IInkAnalyzer**](iinkanalyzer.md) devuelve una colección **IInkAnalysisRecognizers** que contiene los reconocedores de tinta disponibles en el Tablet PC actual.</span><span class="sxs-lookup"><span data-stu-id="6c909-118">The [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method of [**IInkAnalyzer**](iinkanalyzer.md) returns an **IInkAnalysisRecognizers** collection containing the ink recognizers available on the current Tablet PC.</span></span>

<span data-ttu-id="6c909-119">Para un reconocedor de lenguaje, el método [**IInkAnalysisRecognizer:: GetLanguages**](iinkanalysisrecognizer-getlanguages.md) devuelve una matriz no vacía.</span><span class="sxs-lookup"><span data-stu-id="6c909-119">For a language recognizer, the [**IInkAnalysisRecognizer::GetLanguages**](iinkanalysisrecognizer-getlanguages.md) method returns a non-empty array.</span></span> <span data-ttu-id="6c909-120">Para los reconocedores de gestos y los reconocedores de objetos, el método **IInkAnalysisRecognizer:: GetLanguages** devuelve una matriz vacía.</span><span class="sxs-lookup"><span data-stu-id="6c909-120">For both gesture recognizers and object recognizers, the **IInkAnalysisRecognizer::GetLanguages** method returns an empty array.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c909-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c909-121">Requirements</span></span>



| <span data-ttu-id="6c909-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c909-122">Requirement</span></span> | <span data-ttu-id="6c909-123">Value</span><span class="sxs-lookup"><span data-stu-id="6c909-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c909-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c909-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c909-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6c909-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6c909-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c909-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c909-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6c909-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6c909-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c909-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c909-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6c909-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6c909-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c909-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c909-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c909-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6c909-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c909-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c909-133">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="6c909-133">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="6c909-134">**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (método)**</span><span class="sxs-lookup"><span data-stu-id="6c909-134">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="6c909-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="6c909-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

