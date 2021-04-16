---
description: Esta sección contiene información sobre las interfaces y las clases utilizadas en el análisis de tinta. Las clases e interfaces de análisis de tinta no son compatibles con la automatización.
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: Clases e interfaces de análisis de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1c157a08a4b7366c20a712c120265320ab4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539939"
---
# <a name="ink-analysis-classes-and-interfaces"></a><span data-ttu-id="070db-104">Clases e interfaces de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="070db-104">Ink Analysis Classes and Interfaces</span></span>

<span data-ttu-id="070db-105">Esta sección contiene información sobre las interfaces y las clases utilizadas en el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="070db-105">This section contains information about the interfaces and classes used in ink analysis.</span></span> <span data-ttu-id="070db-106">Las clases e interfaces de análisis de tinta no son compatibles con la automatización.</span><span class="sxs-lookup"><span data-stu-id="070db-106">The ink analysis classes and interfaces are not Automation-compliant.</span></span>

## <a name="classes"></a><span data-ttu-id="070db-107">Clases</span><span class="sxs-lookup"><span data-stu-id="070db-107">Classes</span></span>



| <span data-ttu-id="070db-108">Clase</span><span class="sxs-lookup"><span data-stu-id="070db-108">Class</span></span>                                    | <span data-ttu-id="070db-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="070db-109">Description</span></span>                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="070db-110">**AnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="070db-110">**AnalysisRegion**</span></span>](analysisregion.md) | <span data-ttu-id="070db-111">Implementa la interfaz [**IAnalysisRegion**](ianalysisregion.md) .</span><span class="sxs-lookup"><span data-stu-id="070db-111">Implements the [**IAnalysisRegion**](ianalysisregion.md) interface.</span></span><br/> |
| [<span data-ttu-id="070db-112">**InkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="070db-112">**InkAnalyzer**</span></span>](inkanalyzer.md)       | <span data-ttu-id="070db-113">Implementa la interfaz [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="070db-113">Implements the [**IInkAnalyzer**](iinkanalyzer.md) interface.</span></span><br/>       |



 

## <a name="interfaces"></a><span data-ttu-id="070db-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="070db-114">Interfaces</span></span>



| <span data-ttu-id="070db-115">Interfaz</span><span class="sxs-lookup"><span data-stu-id="070db-115">Interface</span></span>                                                    | <span data-ttu-id="070db-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="070db-116">Description</span></span>                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="070db-117">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="070db-117">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)             | <span data-ttu-id="070db-118">Representa las posibles coincidencias de palabras de reconocimiento de escritura a mano para objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="070db-118">Represents the possible handwriting recognition word matches for [**IContextNode**](icontextnode.md) objects.</span></span><br/>                                                                                        |
| [<span data-ttu-id="070db-119">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="070db-119">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)           | <span data-ttu-id="070db-120">Contiene una colección de objetos que implementan la interfaz [**IAnalysisAlternate**](ianalysisalternate.md) y que son el resultado del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="070db-120">Contains a collection of objects that implement the [**IAnalysisAlternate**](ianalysisalternate.md) interface and that are the result of ink analysis.</span></span><br/>                                               |
| [<span data-ttu-id="070db-121">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="070db-121">**IAnalysisRegion**</span></span>](ianalysisregion.md)                   | <span data-ttu-id="070db-122">Expone métodos y propiedades para una región que representa un área de un documento.</span><span class="sxs-lookup"><span data-stu-id="070db-122">Exposes methods and properties for a region that represents an area of a document.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="070db-123">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="070db-123">**IAnalysisStatus**</span></span>](ianalysisstatus.md)                   | <span data-ttu-id="070db-124">Representa el estado de la operación de análisis de tinta al describir si el análisis se completó correctamente y si se produjo alguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="070db-124">Represents the status of the ink analysis operation by describing whether the analysis was completed successfully and whether any warnings occurred.</span></span><br/>                                                  |
| [<span data-ttu-id="070db-125">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="070db-125">**IAnalysisWarning**</span></span>](ianalysiswarning.md)                 | <span data-ttu-id="070db-126">Representa una advertencia o un error que se produce durante una operación de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="070db-126">Represents a warning or error that occurs during an ink analysis operation.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="070db-127">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="070db-127">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)               | <span data-ttu-id="070db-128">Contiene una colección de objetos que implementan la interfaz [**IAnalysisWarning**](ianalysiswarning.md) y que son el resultado de una operación de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="070db-128">Contains a collection of objects that implement the [**IAnalysisWarning**](ianalysiswarning.md) interface and that are the result of an ink analysis operation.</span></span><br/>                                      |
| [<span data-ttu-id="070db-129">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="070db-129">**IContextLink**</span></span>](icontextlink.md)                         | <span data-ttu-id="070db-130">Representa una relación entre dos objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="070db-130">Represents a relationship between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="070db-131">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="070db-131">**IContextLinks**</span></span>](icontextlinks.md)                       | <span data-ttu-id="070db-132">Contiene una colección de objetos que implementan la interfaz [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="070db-132">Contains a collection of objects that implement the [**IContextLink**](icontextlink.md) interface.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="070db-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="070db-133">**IContextNode**</span></span>](icontextnode.md)                         | <span data-ttu-id="070db-134">Representa un nodo en un árbol de objetos que se crean como parte del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="070db-134">Represents a node in a tree of objects that are created as part of ink analysis.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="070db-135">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="070db-135">**IContextNodes**</span></span>](icontextnodes.md)                       | <span data-ttu-id="070db-136">Contiene una colección de objetos que implementan la interfaz [**IContextNode**](icontextnode.md) y que son el resultado de una operación de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="070db-136">Contains a collection of objects that implement the [**IContextNode**](icontextnode.md) interface and that are the result of an ink analysis operation.</span></span><br/>                                              |
| [<span data-ttu-id="070db-137">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="070db-137">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)     | <span data-ttu-id="070db-138">Proporciona acceso a los reconocedores de escritura a mano para su uso con el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="070db-138">Provides access to handwriting recognizers for use with ink analysis.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="070db-139">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="070db-139">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)   | <span data-ttu-id="070db-140">Contiene una colección de objetos que implementan la interfaz [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) y que representan la capacidad de reconocer escritura a mano, objetos o gestos.</span><span class="sxs-lookup"><span data-stu-id="070db-140">Contains a collection of objects that implement the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) interface and that represent the ability to recognize handwriting, objects, or gestures.</span></span><br/> |
| [<span data-ttu-id="070db-141">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="070db-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)                         | <span data-ttu-id="070db-142">Proporciona acceso al análisis de diseño, la clasificación de escritura y de dibujo y el reconocimiento de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="070db-142">Provides access to layout analysis, writing and drawing classification, and handwriting recognition.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="070db-143">**IMatchesCriteriaCallBack**</span><span class="sxs-lookup"><span data-stu-id="070db-143">**IMatchesCriteriaCallBack**</span></span>](imatchescriteriacallback.md) | <span data-ttu-id="070db-144">Expone un método para evaluar si un objeto [**IContextNode**](icontextnode.md) cumple o no los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="070db-144">Exposes a method to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails a specified criteria.</span></span><br/>                                                                              |



 

## <a name="return-values"></a><span data-ttu-id="070db-145">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="070db-145">Return Values</span></span>

<span data-ttu-id="070db-146">Los métodos de la biblioteca COM de Tablet PC devuelven los valores **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="070db-146">Methods in the Tablet PC COM Library return values of **HRESULT**.</span></span> <span data-ttu-id="070db-147">A menos que se indique lo contrario, en esta tabla se describen los significados de los valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="070db-147">Unless otherwise noted, the meanings of the **HRESULT** values are described in this table.</span></span>



| <span data-ttu-id="070db-148">Valor HRESULT</span><span class="sxs-lookup"><span data-stu-id="070db-148">HRESULT value</span></span>                                   | <span data-ttu-id="070db-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="070db-149">Description</span></span>                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="070db-150">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="070db-150">S\_OK</span></span><br/>                                | <span data-ttu-id="070db-151">Correcto.</span><span class="sxs-lookup"><span data-stu-id="070db-151">Success.</span></span><br/>                                                                      |
| <span data-ttu-id="070db-152">\_puntero E</span><span class="sxs-lookup"><span data-stu-id="070db-152">E\_POINTER</span></span><br/>                           | <span data-ttu-id="070db-153">Al menos un puntero (para un parámetro de entrada o de salida) no es válido.</span><span class="sxs-lookup"><span data-stu-id="070db-153">At least one pointer (for either an input or an output parameter) is invalid.</span></span><br/> |
| <span data-ttu-id="070db-154">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="070db-154">E\_INVALIDARG</span></span><br/>                        | <span data-ttu-id="070db-155">El miembro intentó pasar un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="070db-155">Member attempted to pass in an invalid argument.</span></span><br/>                              |
| <span data-ttu-id="070db-156">\_excepción de entrada manuscrita \_</span><span class="sxs-lookup"><span data-stu-id="070db-156">E\_INK\_EXCEPTION</span></span><br/>                    | <span data-ttu-id="070db-157">Se produjo una excepción.</span><span class="sxs-lookup"><span data-stu-id="070db-157">Exception occurred.</span></span><br/>                                                           |
| <span data-ttu-id="070db-158">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="070db-158">E\_OUTOFMEMORY</span></span><br/>                       | <span data-ttu-id="070db-159">El sistema no puede asignar memoria para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="070db-159">System cannot allocate memory to complete the operation.</span></span><br/>                      |
| <span data-ttu-id="070db-160">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="070db-160">E\_FAIL</span></span><br/>                              | <span data-ttu-id="070db-161">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="070db-161">Unspecified failure occurred.</span></span><br/>                                                 |
| <span data-ttu-id="070db-162">E \_ INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="070db-162">E\_INVALIDOPERATION</span></span><br/>                  | <span data-ttu-id="070db-163">El miembro intentó usar una operación no válida.</span><span class="sxs-lookup"><span data-stu-id="070db-163">Member attempted to use an invalid operation.</span></span><br/>                                 |
| <span data-ttu-id="070db-164">TPC \_ E \_ modo no válido \_</span><span class="sxs-lookup"><span data-stu-id="070db-164">TPC\_E\_INVALID\_MODE</span></span><br/>                | <span data-ttu-id="070db-165">El miembro intentó utilizar un modo no válido.</span><span class="sxs-lookup"><span data-stu-id="070db-165">Member attempted to use an invalid mode.</span></span><br/>                                      |
| <span data-ttu-id="070db-166">\_ \_ configuración no válida de TPC E \_</span><span class="sxs-lookup"><span data-stu-id="070db-166">TPC\_E\_INVALID\_CONFIGURATION</span></span><br/>       | <span data-ttu-id="070db-167">El miembro intentó usar una configuración no válida.</span><span class="sxs-lookup"><span data-stu-id="070db-167">Member attempted to use an invalid configuration.</span></span><br/>                             |
| <span data-ttu-id="070db-168">\_Descripción de \_ paquetes no válidos de TPC E \_ \_</span><span class="sxs-lookup"><span data-stu-id="070db-168">TPC\_E\_INVALID\_PACKET\_DESCRIPTION</span></span><br/> | <span data-ttu-id="070db-169">El miembro intentó usar una descripción de paquete no válida.</span><span class="sxs-lookup"><span data-stu-id="070db-169">Member attempted to use an invalid packet description.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="070db-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="070db-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="070db-171">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="070db-171">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




