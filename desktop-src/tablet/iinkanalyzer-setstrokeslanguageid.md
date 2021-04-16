---
description: Cambia el identificador de configuración regional para los trazos especificados.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: 'IInkAnalyzer:: SetStrokesLanguageId (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84d2e4b9e3ac24fc73eddc4f84bcc9337cb4c372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705694"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a><span data-ttu-id="79211-103">IInkAnalyzer:: SetStrokesLanguageId (método)</span><span class="sxs-lookup"><span data-stu-id="79211-103">IInkAnalyzer::SetStrokesLanguageId method</span></span>

<span data-ttu-id="79211-104">Cambia el identificador de configuración regional para los trazos especificados.</span><span class="sxs-lookup"><span data-stu-id="79211-104">Changes the locale identifier for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="79211-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79211-105">Syntax</span></span>


```C++
HRESULT SetStrokesLanguageId(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes,
  [in] LONG  lStrokesLCID
);
```



## <a name="parameters"></a><span data-ttu-id="79211-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79211-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79211-107">*ulStrokeIdCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79211-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79211-108">Número de identificadores de trazo en *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="79211-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="79211-109">*plStrokes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79211-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79211-110">Matriz de identificadores para los trazos a los que se va a asignar el identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="79211-110">The array of identifiers for the strokes to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="79211-111">*lStrokesLCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79211-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79211-112">Identificador de configuración regional que se va a asignar a los trazos.</span><span class="sxs-lookup"><span data-stu-id="79211-112">The locale identifier to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79211-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79211-113">Return value</span></span>

<span data-ttu-id="79211-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="79211-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="79211-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79211-115">Remarks</span></span>

<span data-ttu-id="79211-116">La configuración regional de un trazo se establece al agregar el trazo mediante una llamada al método [**IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md), el método [**IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="79211-116">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="79211-117">Para obtener la configuración regional asignada actualmente a un trazo, llame al [**método IInkAnalyzer:: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="79211-117">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="79211-118">Los trazos especificados se mueven a un nodo de tinta sin clasificar (vea [**IContextNode:: GetType**](icontextnode-gettype.md)) que contiene los trazos del mismo idioma.</span><span class="sxs-lookup"><span data-stu-id="79211-118">The specified strokes are moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="79211-119">Si no existe tal [**IContextNode**](icontextnode.md) , este método crea un nuevo nodo de tinta sin clasificar y le mueve los trazos.</span><span class="sxs-lookup"><span data-stu-id="79211-119">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the strokes to it.</span></span> <span data-ttu-id="79211-120">Un nodo de tinta sin clasificar es un **IContextNode** que tiene un tipo de UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="79211-120">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="79211-121">Si este método mueve trazos de un [**IContextNode**](icontextnode.md) que no es un nodo de tinta sin clasificar, este método también agrega los cuadros de límite de los trazos a la región desfasada del analizador de tinta (vea el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="79211-121">If this method moves strokes from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the strokes' bounding boxes to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="79211-122">Este método no mueve un trazo si el parámetro *lStrokeLCID* coincide con el identificador de idioma actual del trazo.</span><span class="sxs-lookup"><span data-stu-id="79211-122">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="79211-123">Si un trazo especificado no está asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método omite el identificador.</span><span class="sxs-lookup"><span data-stu-id="79211-123">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="79211-124">Si ninguno de los trazos especificados identifica un trazo asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="79211-124">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="79211-125">Este método devuelve un código de error cuando strokeIds es **null**.</span><span class="sxs-lookup"><span data-stu-id="79211-125">This method returns an error code when strokeIds is **NULL**.</span></span>

<span data-ttu-id="79211-126">Para obtener más información sobre los identificadores de idioma, vea [constantes y cadenas de identificador de idioma](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="79211-126">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="79211-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79211-127">Requirements</span></span>



| <span data-ttu-id="79211-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="79211-128">Requirement</span></span> | <span data-ttu-id="79211-129">Value</span><span class="sxs-lookup"><span data-stu-id="79211-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79211-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79211-130">Minimum supported client</span></span><br/> | <span data-ttu-id="79211-131">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="79211-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="79211-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79211-132">Minimum supported server</span></span><br/> | <span data-ttu-id="79211-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="79211-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="79211-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79211-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="79211-135"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="79211-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="79211-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79211-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79211-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79211-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="79211-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="79211-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79211-139">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="79211-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="79211-140">**IInkAnalyzer:: AddStroke (método)**</span><span class="sxs-lookup"><span data-stu-id="79211-140">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="79211-141">**IInkAnalyzer:: AddStrokeForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="79211-141">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="79211-142">**IInkAnalyzer:: AddStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="79211-142">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="79211-143">**IInkAnalyzer:: AddStrokesForLanguage (método)**</span><span class="sxs-lookup"><span data-stu-id="79211-143">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="79211-144">**IInkAnalyzer:: GetStrokeLanguageId (método)**</span><span class="sxs-lookup"><span data-stu-id="79211-144">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="79211-145">**IInkAnalyzer:: SetStrokeLanguageId (método)**</span><span class="sxs-lookup"><span data-stu-id="79211-145">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="79211-146">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="79211-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

