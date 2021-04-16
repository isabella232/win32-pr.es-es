---
description: Proporciona acceso a los reconocedores de escritura a mano para su uso con el análisis de tinta.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Interfaz IInkAnalysisRecognizer (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b091b47d14929e155548dc057ef0fdb1731133a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696526"
---
# <a name="iinkanalysisrecognizer-interface"></a><span data-ttu-id="579a6-103">Interfaz IInkAnalysisRecognizer</span><span class="sxs-lookup"><span data-stu-id="579a6-103">IInkAnalysisRecognizer interface</span></span>

<span data-ttu-id="579a6-104">Proporciona acceso a los reconocedores de escritura a mano para su uso con el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="579a6-104">Provides access to handwriting recognizers for use with ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="579a6-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="579a6-105">Members</span></span>

<span data-ttu-id="579a6-106">La interfaz **IInkAnalysisRecognizer** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="579a6-106">The **IInkAnalysisRecognizer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="579a6-107">**IInkAnalysisRecognizer** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="579a6-107">**IInkAnalysisRecognizer** also has these types of members:</span></span>

-   [<span data-ttu-id="579a6-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="579a6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="579a6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="579a6-109">Methods</span></span>

<span data-ttu-id="579a6-110">La interfaz **IInkAnalysisRecognizer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="579a6-110">The **IInkAnalysisRecognizer** interface has these methods.</span></span>



| <span data-ttu-id="579a6-111">Método</span><span class="sxs-lookup"><span data-stu-id="579a6-111">Method</span></span>                                                                          | <span data-ttu-id="579a6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="579a6-112">Description</span></span>                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="579a6-113">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="579a6-113">**GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)               | <span data-ttu-id="579a6-114">Recupera las capacidades del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="579a6-114">Retrieves the capabilities of the recognizer.</span></span><br/>                                                                       |
| [<span data-ttu-id="579a6-115">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="579a6-115">**GetGuid**</span></span>](iinkanalysisrecognizer-getguid.md)                               | <span data-ttu-id="579a6-116">Recupera el identificador único global (GUID) del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="579a6-116">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span><br/>                                                  |
| [<span data-ttu-id="579a6-117">**GetLanguages**</span><span class="sxs-lookup"><span data-stu-id="579a6-117">**GetLanguages**</span></span>](iinkanalysisrecognizer-getlanguages.md)                     | <span data-ttu-id="579a6-118">Recupera los identificadores de las configuraciones regionales admitidas por este **IInkAnalysisRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="579a6-118">Retrieves the identifiers for the locales that this **IInkAnalysisRecognizer** supports.</span></span><br/>                            |
| [<span data-ttu-id="579a6-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="579a6-119">**GetName**</span></span>](iinkanalysisrecognizer-getname.md)                               | <span data-ttu-id="579a6-120">Recupera el nombre del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="579a6-120">Retrieves the name of the recognizer.</span></span><br/>                                                                               |
| [<span data-ttu-id="579a6-121">**GetSupportedProperties**</span><span class="sxs-lookup"><span data-stu-id="579a6-121">**GetSupportedProperties**</span></span>](iinkanalysisrecognizer-getsupportedproperties.md) | <span data-ttu-id="579a6-122">Recupera los identificadores únicos globales (GUID) de las propiedades que admite este **IInkAnalysisRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="579a6-122">Retrieves the globally unique identifiers (GUIDs) for the properties that this **IInkAnalysisRecognizer** supports.</span></span><br/> |
| [<span data-ttu-id="579a6-123">**GetVendor**</span><span class="sxs-lookup"><span data-stu-id="579a6-123">**GetVendor**</span></span>](iinkanalysisrecognizer-getvendor.md)                           | <span data-ttu-id="579a6-124">Recupera el nombre del proveedor de **IInkAnalysisRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="579a6-124">Retrieves the vendor name of the **IInkAnalysisRecognizer**.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="579a6-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="579a6-125">Remarks</span></span>

<span data-ttu-id="579a6-126">Un reconocedor tiene atributos y propiedades específicos que permiten realizar el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="579a6-126">A recognizer has specific attributes and properties that allow it to perform recognition.</span></span> <span data-ttu-id="579a6-127">Las propiedades de un reconocedor deben determinarse antes de que se pueda realizar el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="579a6-127">The properties of a recognizer must be determined before recognition can occur.</span></span> <span data-ttu-id="579a6-128">Los tipos de propiedades que admite un reconocedor determinan los tipos de reconocimiento que puede realizar.</span><span class="sxs-lookup"><span data-stu-id="579a6-128">The types of properties that a recognizer supports determine the types of recognition that it can perform.</span></span> <span data-ttu-id="579a6-129">Por ejemplo, si un reconocedor no admite la escritura a mano cursiva, devuelve resultados inexactos cuando un usuario escribe en cursiva.</span><span class="sxs-lookup"><span data-stu-id="579a6-129">For instance, if a recognizer does not support cursive handwriting, it returns inaccurate results when a user writes in cursive.</span></span>

<span data-ttu-id="579a6-130">Un reconocedor también tiene una funcionalidad integrada que administra automáticamente muchos aspectos de la escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="579a6-130">A recognizer also has built-in functionality that automatically manages many aspects of handwriting.</span></span> <span data-ttu-id="579a6-131">Por ejemplo, determina las métricas de las líneas en las que se dibujan los trazos.</span><span class="sxs-lookup"><span data-stu-id="579a6-131">For instance, it determines the metrics for the lines on which strokes are drawn.</span></span> <span data-ttu-id="579a6-132">Puede devolver el número de línea de un trazo, pero nunca necesita especificar cómo se determinan esas métricas de línea debido a la funcionalidad integrada del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="579a6-132">You can return the line number of a stroke, but you never need to specify how those line metrics are determined because of the built-in functionality of the recognizer.</span></span>

<span data-ttu-id="579a6-133">[**IInkAnalyzer**](iinkanalyzer.md) mantiene una lista de los reconocedores disponibles.</span><span class="sxs-lookup"><span data-stu-id="579a6-133">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a list of available recognizers.</span></span> <span data-ttu-id="579a6-134">Para tener acceso a esta lista, use el método [**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) .</span><span class="sxs-lookup"><span data-stu-id="579a6-134">To access this list, use the [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="579a6-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="579a6-135">Requirements</span></span>



| <span data-ttu-id="579a6-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="579a6-136">Requirement</span></span> | <span data-ttu-id="579a6-137">Value</span><span class="sxs-lookup"><span data-stu-id="579a6-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="579a6-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="579a6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="579a6-139">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="579a6-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="579a6-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="579a6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="579a6-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="579a6-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="579a6-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="579a6-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="579a6-143"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="579a6-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="579a6-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="579a6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="579a6-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="579a6-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="579a6-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="579a6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579a6-147">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="579a6-147">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="579a6-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="579a6-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="579a6-149">**IInkAnalyzer:: CreateCustomRecognizer (método)**</span><span class="sxs-lookup"><span data-stu-id="579a6-149">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="579a6-150">Tipos de nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="579a6-150">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="579a6-151">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="579a6-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

