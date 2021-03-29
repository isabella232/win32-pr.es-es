---
description: Cambia el identificador de configuración regional del trazo especificado.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: 'IInkAnalyzer:: SetStrokeLanguageId (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e103683d85ff971a8f0daff2574e97672dd5a84b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541990"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a><span data-ttu-id="d3e05-103">IInkAnalyzer:: SetStrokeLanguageId (método)</span><span class="sxs-lookup"><span data-stu-id="d3e05-103">IInkAnalyzer::SetStrokeLanguageId method</span></span>

<span data-ttu-id="d3e05-104">Cambia el identificador de configuración regional del trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="d3e05-104">Changes the locale identifier for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e05-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3e05-105">Syntax</span></span>


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="d3e05-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3e05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3e05-107">*lStrokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d3e05-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3e05-108">Identificador del trazo al que se va a asignar el identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="d3e05-108">The identifier of the stroke to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d3e05-109">*lStrokeLCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d3e05-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3e05-110">Identificador de configuración regional que se va a asignar al trazo.</span><span class="sxs-lookup"><span data-stu-id="d3e05-110">The locale identifier to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3e05-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3e05-111">Return value</span></span>

<span data-ttu-id="d3e05-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d3e05-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d3e05-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3e05-113">Remarks</span></span>

<span data-ttu-id="d3e05-114">La configuración regional de un trazo se establece al agregar el trazo mediante una llamada al método [**IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md), el método [**IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="d3e05-114">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="d3e05-115">Para obtener la configuración regional asignada actualmente a un trazo, llame al [**método IInkAnalyzer:: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="d3e05-115">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="d3e05-116">El trazo especificado se mueve a un nodo de tinta sin clasificar (vea [**IContextNode:: GetType**](icontextnode-gettype.md)) que contiene los trazos del mismo idioma.</span><span class="sxs-lookup"><span data-stu-id="d3e05-116">The specified stroke is moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="d3e05-117">Si no existe tal [**IContextNode**](icontextnode.md) , este método crea un nuevo nodo de tinta sin clasificar y le mueve el trazo.</span><span class="sxs-lookup"><span data-stu-id="d3e05-117">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the stroke to it.</span></span> <span data-ttu-id="d3e05-118">Un nodo de tinta sin clasificar es un **IContextNode** que tiene un tipo de UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="d3e05-118">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="d3e05-119">Si este método mueve un trazo desde un [**IContextNode**](icontextnode.md) que no es un nodo de tinta no clasificado, este método también agrega el rectángulo de selección del trazo a la región desfasada del analizador de tinta (vea el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="d3e05-119">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="d3e05-120">Este método no mueve un trazo si el parámetro *lStrokeLCID* coincide con el identificador de idioma actual del trazo.</span><span class="sxs-lookup"><span data-stu-id="d3e05-120">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="d3e05-121">Si el trazo especificado no está asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="d3e05-121">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="d3e05-122">Para obtener más información sobre los identificadores de idioma, vea [constantes y cadenas de identificador de idioma](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="d3e05-122">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e05-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3e05-123">Requirements</span></span>



| <span data-ttu-id="d3e05-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3e05-124">Requirement</span></span> | <span data-ttu-id="d3e05-125">Value</span><span class="sxs-lookup"><span data-stu-id="d3e05-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e05-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3e05-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e05-127">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d3e05-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d3e05-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3e05-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e05-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d3e05-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d3e05-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3e05-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e05-131"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d3e05-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d3e05-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d3e05-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3e05-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3e05-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d3e05-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3e05-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e05-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d3e05-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d3e05-136">**IInkAnalyzer:: AddStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="d3e05-136">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="d3e05-137">**IInkAnalyzer:: AddStrokeForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="d3e05-137">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="d3e05-138">**IInkAnalyzer:: AddStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="d3e05-138">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="d3e05-139">**IInkAnalyzer:: AddStrokesForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="d3e05-139">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="d3e05-140">**IInkAnalyzer:: GetStrokeLanguageId (método)**</span><span class="sxs-lookup"><span data-stu-id="d3e05-140">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="d3e05-141">**IInkAnalyzer:: SetStrokesLanguageId (método)**</span><span class="sxs-lookup"><span data-stu-id="d3e05-141">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="d3e05-142">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="d3e05-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

