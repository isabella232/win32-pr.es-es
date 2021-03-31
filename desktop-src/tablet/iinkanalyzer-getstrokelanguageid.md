---
description: Devuelve el identificador de configuración regional del trazo especificado.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'IInkAnalyzer:: GetStrokeLanguageId (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810003"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a><span data-ttu-id="825e0-103">IInkAnalyzer:: GetStrokeLanguageId (método)</span><span class="sxs-lookup"><span data-stu-id="825e0-103">IInkAnalyzer::GetStrokeLanguageId method</span></span>

<span data-ttu-id="825e0-104">Devuelve el identificador de configuración regional del trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="825e0-104">Returns the locale identifier of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="825e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="825e0-105">Syntax</span></span>


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="825e0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="825e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="825e0-107">*lStrokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="825e0-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="825e0-108">Identificador del trazo.</span><span class="sxs-lookup"><span data-stu-id="825e0-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="825e0-109">*lStrokeLCID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="825e0-109">*lStrokeLCID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="825e0-110">Identificador de configuración regional del trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="825e0-110">The locale identifier for the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="825e0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="825e0-111">Return value</span></span>

<span data-ttu-id="825e0-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="825e0-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="825e0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="825e0-113">Remarks</span></span>

<span data-ttu-id="825e0-114">La configuración regional del trazo se establece al agregar el trazo mediante una llamada al método [**IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md), el método [**IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="825e0-114">The stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="825e0-115">Para cambiar la configuración regional del trazo, use el método [**IInkAnalyzer:: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md) o [**IInkAnalyzer:: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="825e0-115">To change the stroke's locale, use [**IInkAnalyzer::SetStrokeLanguageId Method**](iinkanalyzer-setstrokelanguageid.md) or [**IInkAnalyzer::SetStrokesLanguageId Method**](iinkanalyzer-setstrokeslanguageid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="825e0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="825e0-116">Requirements</span></span>



| <span data-ttu-id="825e0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="825e0-117">Requirement</span></span> | <span data-ttu-id="825e0-118">Value</span><span class="sxs-lookup"><span data-stu-id="825e0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="825e0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="825e0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="825e0-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="825e0-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="825e0-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="825e0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="825e0-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="825e0-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="825e0-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="825e0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="825e0-124"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="825e0-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="825e0-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="825e0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="825e0-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="825e0-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="825e0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="825e0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="825e0-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="825e0-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="825e0-129">**IInkAnalyzer:: SetStrokeLanguageId (método)**</span><span class="sxs-lookup"><span data-stu-id="825e0-129">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="825e0-130">**IInkAnalyzer:: SetStrokesLanguageId (método)**</span><span class="sxs-lookup"><span data-stu-id="825e0-130">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="825e0-131">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="825e0-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




