---
description: 'Aplica los resultados de una operación de análisis de tinta de fondo en el árbol de nodos de contexto para las partes del árbol que no ha sido modificada por la aplicación desde la llamada al método IInkAnalyzer:: BackgroundAnalyze.'
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'IInkAnalyzer:: reconcile (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33229c7da47f294f317d2216d9e9bf4f6b114599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648205"
---
# <a name="iinkanalyzerreconcile-method"></a><span data-ttu-id="34bf1-103">IInkAnalyzer:: reconciliate (método)</span><span class="sxs-lookup"><span data-stu-id="34bf1-103">IInkAnalyzer::Reconcile method</span></span>

<span data-ttu-id="34bf1-104">Aplica los resultados de una operación de análisis de tinta de fondo en el árbol de nodos de contexto para las partes del árbol que no ha sido modificada por la aplicación desde la llamada al [**método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="34bf1-104">Applies the results of a background ink analysis operation to the context node tree for the portions of the tree that have not been modified by the application since the call to [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="34bf1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34bf1-105">Syntax</span></span>


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a><span data-ttu-id="34bf1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34bf1-106">Parameters</span></span>

<span data-ttu-id="34bf1-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="34bf1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="34bf1-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34bf1-108">Return value</span></span>

<span data-ttu-id="34bf1-109">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="34bf1-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="34bf1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34bf1-110">Remarks</span></span>

<span data-ttu-id="34bf1-111">De forma predeterminada, el [**IInkAnalyzer**](iinkanalyzer.md) realiza una fase de conciliación automática inmediatamente antes de generar los eventos [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) y [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="34bf1-111">By default, the [**IInkAnalyzer**](iinkanalyzer.md) performs an automatic reconciliation phase immediately before raising the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) and [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) events.</span></span>

<span data-ttu-id="34bf1-112">Para deshabilitar la reconciliación automática, desactive la marca **AnalysisModes \_ AutomaticReconciliation** de los modos de análisis del analizador de tinta (consulte [**IInkAnalyzer:: SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md) y [**AnalysisModes**](analysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="34bf1-112">To disable automatic reconciliation, clear the **AnalysisModes\_AutomaticReconciliation** flag from the ink analyzer's analysis modes (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md) and [**AnalysisModes**](analysismodes.md)).</span></span> <span data-ttu-id="34bf1-113">El método [**IInkAnalyzer:: BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) devuelve un error cuando la reconciliación automática está deshabilitada y la aplicación no controla el evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="34bf1-113">The [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method returns an error when automatic reconciliation is disabled and your application does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="34bf1-114">La aplicación debe llamar al método de **método IInkAnalyzer:: Reconciliate** para que [**IInkAnalyzer**](iinkanalyzer.md) pueda continuar procesando los resultados o continuar el análisis de la fase de análisis correspondiente.</span><span class="sxs-lookup"><span data-stu-id="34bf1-114">Your application must call the **IInkAnalyzer::Reconcile Method** method before the [**IInkAnalyzer**](iinkanalyzer.md) can continue to process the results or continue further analysis for the corresponding analysis stage.</span></span>

<span data-ttu-id="34bf1-115">La aplicación puede realizar cambios, como agregar o quitar trazos y cambiar los datos del trazo, en el árbol de nodos de contexto del objeto [**IInkAnalyzer**](iinkanalyzer.md) durante el análisis en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="34bf1-115">Your application can make changes, such as adding or removing strokes and changing stroke data, in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree during background analysis.</span></span> <span data-ttu-id="34bf1-116">Estos cambios pueden invalidar partes de los resultados del análisis en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="34bf1-116">Such changes can invalidate portions of the background analysis results.</span></span> <span data-ttu-id="34bf1-117">Este método aplica solo los resultados del análisis al árbol de nodos de contexto del analizador para las partes del árbol que la aplicación no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="34bf1-117">This method applies analysis results only to the analyzer's context node tree for the portions of the tree that your application has not changed.</span></span> <span data-ttu-id="34bf1-118">Este método también agrega regiones que contienen resultados de análisis invalidados a la región desfasada del objeto **IInkAnalyzer** (vea el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="34bf1-118">This method also adds regions containing invalidated analysis results to the **IInkAnalyzer** object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="34bf1-119">Para obtener más información acerca del uso de para analizar la entrada manuscrita, consulte [información general del análisis de tinta](ink-analysis-overview.md). [**AnalysisModes**](analysismodes.md)</span><span class="sxs-lookup"><span data-stu-id="34bf1-119">For more information about using the to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).[**AnalysisModes**](analysismodes.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="34bf1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34bf1-120">Requirements</span></span>



| <span data-ttu-id="34bf1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="34bf1-121">Requirement</span></span> | <span data-ttu-id="34bf1-122">Value</span><span class="sxs-lookup"><span data-stu-id="34bf1-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34bf1-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34bf1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="34bf1-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="34bf1-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="34bf1-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34bf1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="34bf1-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="34bf1-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="34bf1-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34bf1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="34bf1-128"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="34bf1-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="34bf1-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34bf1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34bf1-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34bf1-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="34bf1-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="34bf1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34bf1-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="34bf1-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="34bf1-133">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="34bf1-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="34bf1-134">**\_IAnalysisEvents::ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="34bf1-134">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="34bf1-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="34bf1-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




