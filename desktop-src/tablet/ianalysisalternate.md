---
description: Representa las posibles coincidencias de palabras de reconocimiento de escritura a mano para objetos IContextNode.
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: Interfaz IAnalysisAlternate (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275489"
---
# <a name="ianalysisalternate-interface"></a><span data-ttu-id="1847d-103">Interfaz IAnalysisAlternate</span><span class="sxs-lookup"><span data-stu-id="1847d-103">IAnalysisAlternate interface</span></span>

<span data-ttu-id="1847d-104">Representa las posibles coincidencias de palabras de reconocimiento de escritura a mano para objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="1847d-104">Represents the possible handwriting recognition word matches for [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="1847d-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="1847d-105">Members</span></span>

<span data-ttu-id="1847d-106">La interfaz **IAnalysisAlternate** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1847d-106">The **IAnalysisAlternate** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1847d-107">**IAnalysisAlternate** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1847d-107">**IAnalysisAlternate** also has these types of members:</span></span>

-   [<span data-ttu-id="1847d-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="1847d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1847d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1847d-109">Methods</span></span>

<span data-ttu-id="1847d-110">La interfaz **IAnalysisAlternate** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1847d-110">The **IAnalysisAlternate** interface has these methods.</span></span>



| <span data-ttu-id="1847d-111">Método</span><span class="sxs-lookup"><span data-stu-id="1847d-111">Method</span></span>                                                                          | <span data-ttu-id="1847d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1847d-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1847d-113">**GetAlternateNodes**</span><span class="sxs-lookup"><span data-stu-id="1847d-113">**GetAlternateNodes**</span></span>](ianalysisalternate-getalternatenodes.md)               | <span data-ttu-id="1847d-114">Recupera los objetos [**IContextNode**](icontextnode.md) asociados a esta alternativa.</span><span class="sxs-lookup"><span data-stu-id="1847d-114">Retrieves the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span><br/>                                                       |
| [<span data-ttu-id="1847d-115">**GetRecognitionConfidence**</span><span class="sxs-lookup"><span data-stu-id="1847d-115">**GetRecognitionConfidence**</span></span>](ianalysisalternate-getrecognitionconfidence.md) | <span data-ttu-id="1847d-116">Recupera un valor que indica el nivel de confianza que [**IInkAnalyzer**](iinkanalyzer.md) tiene en la precisión de **IAnalysisAlternate**.</span><span class="sxs-lookup"><span data-stu-id="1847d-116">Retrieves a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the **IAnalysisAlternate**.</span></span><br/> |
| [<span data-ttu-id="1847d-117">**GetRecognizedString**</span><span class="sxs-lookup"><span data-stu-id="1847d-117">**GetRecognizedString**</span></span>](ianalysisalternate-getrecognizedstring.md)           | <span data-ttu-id="1847d-118">Recupera el valor de cadena reconocido del objeto **IAnalysisAlternate** .</span><span class="sxs-lookup"><span data-stu-id="1847d-118">Retrieves the recognized string value of the **IAnalysisAlternate** object.</span></span><br/>                                                                               |
| [<span data-ttu-id="1847d-119">**GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="1847d-119">**GetStrokeIds**</span></span>](ianalysisalternate-getstrokeids.md)                         | <span data-ttu-id="1847d-120">Recupera los identificadores de trazo asociados a este **IAnalysisAlternate**.</span><span class="sxs-lookup"><span data-stu-id="1847d-120">Retrieves the stroke identifiers that are associated with this **IAnalysisAlternate**.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="1847d-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1847d-121">Remarks</span></span>

<span data-ttu-id="1847d-122">Hay muchas variaciones en la escritura a mano de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1847d-122">There are many variations in users' handwriting.</span></span> <span data-ttu-id="1847d-123">Por ese motivo, los reconocedores de escritura a mano a veces pueden convertir la escritura a mano en texto diferente del previsto por el usuario.</span><span class="sxs-lookup"><span data-stu-id="1847d-123">For that reason, handwriting recognizers can sometimes convert handwriting into text that is different from what the user intended.</span></span> <span data-ttu-id="1847d-124">Cuando un [**IInkAnalyzer**](iinkanalyzer.md) realiza un análisis en una colección de trazos, el **IInkAnalyzer** busca el conjunto de palabras más probable que representa la escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="1847d-124">When an [**IInkAnalyzer**](iinkanalyzer.md) performs analysis on a collection of strokes, the **IInkAnalyzer** finds the most likely set of words that the handwriting represents.</span></span> <span data-ttu-id="1847d-125">Además, **IInkAnalyzer** también encuentra conjuntos de coincidencias de reconocimiento alternativas, que se almacenan en una colección [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="1847d-125">In addition, the **IInkAnalyzer** also finds sets of alternative recognition matches, which are stored in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span> <span data-ttu-id="1847d-126">Para que un usuario pueda aprovechar las alternativas de reconocimiento, debe crear una interfaz de usuario que permita al usuario seleccionar el **IAnalysisAlternate** correcto.</span><span class="sxs-lookup"><span data-stu-id="1847d-126">In order for a user to take advantage of recognition alternates, you must create a user interface that allows the user to select the correct **IAnalysisAlternate**.</span></span>

<span data-ttu-id="1847d-127">Los objetos **IAnalysisAlternate** se obtienen generalmente a través del [**método IInkAnalyzer:: GetAlternates**](iinkanalyzer-getalternates.md).</span><span class="sxs-lookup"><span data-stu-id="1847d-127">**IAnalysisAlternate** objects are generally obtained through [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md).</span></span> <span data-ttu-id="1847d-128">El primer objeto **IAnalysisAlternate** de la colección es lo que el [**IInkAnalyzer**](iinkanalyzer.md) considera como la alternativa más probable.</span><span class="sxs-lookup"><span data-stu-id="1847d-128">The first **IAnalysisAlternate** object in the collection is what the [**IInkAnalyzer**](iinkanalyzer.md) considers to be the most likely alternate.</span></span>

<span data-ttu-id="1847d-129">Esta interfaz es equivalente a [System. Windows. Ink. AnalysisCore. AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) en el .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="1847d-129">This interface is equivalent to [System.Windows.Ink.AnalysisCore.AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="1847d-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1847d-130">Requirements</span></span>



| <span data-ttu-id="1847d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1847d-131">Requirement</span></span> | <span data-ttu-id="1847d-132">Value</span><span class="sxs-lookup"><span data-stu-id="1847d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1847d-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1847d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1847d-134">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1847d-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1847d-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1847d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1847d-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1847d-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1847d-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1847d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1847d-138"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1847d-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1847d-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1847d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1847d-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1847d-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1847d-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="1847d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1847d-142">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="1847d-142">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="1847d-143">**IInkAnalyzer:: GetAlternatesForContextNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="1847d-143">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="1847d-144">**IInkAnalyzer:: GetAlternatesForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="1847d-144">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="1847d-145">**IInkAnalyzer:: GetAlternates (método)**</span><span class="sxs-lookup"><span data-stu-id="1847d-145">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="1847d-146">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="1847d-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

