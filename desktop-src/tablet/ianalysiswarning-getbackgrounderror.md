---
description: Recupera el código de error de la operación de análisis de tinta de fondo si se produce un error.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'IAnalysisWarning:: GetBackgroundError (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4367b1d52ee5d2a3bb65af0e4edd4922b8ae9a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275483"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a><span data-ttu-id="da4f0-103">IAnalysisWarning:: GetBackgroundError (método)</span><span class="sxs-lookup"><span data-stu-id="da4f0-103">IAnalysisWarning::GetBackgroundError method</span></span>

<span data-ttu-id="da4f0-104">Recupera el código de error de la operación de análisis de tinta de fondo si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="da4f0-104">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="da4f0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da4f0-105">Syntax</span></span>


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a><span data-ttu-id="da4f0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da4f0-106">Parameters</span></span>

<span data-ttu-id="da4f0-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="da4f0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da4f0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da4f0-108">Return value</span></span>

<span data-ttu-id="da4f0-109">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="da4f0-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="da4f0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da4f0-110">Remarks</span></span>

<span data-ttu-id="da4f0-111">Si se produce un error en una operación de análisis en segundo plano, el [**IInkAnalyzer**](iinkanalyzer.md) no puede devolver el código de error porque se está produciendo en un subproceso diferente.</span><span class="sxs-lookup"><span data-stu-id="da4f0-111">If an error occurs within a background analysis operation, the [**IInkAnalyzer**](iinkanalyzer.md) cannot return the error code because it is occurring in a different thread.</span></span> <span data-ttu-id="da4f0-112">En su lugar, el controlador de eventos [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) recibe un [**IAnalysisStatus**](ianalysisstatus.md) que contiene un [**IAnalysisWarning**](ianalysiswarning.md) con un [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ BackgroundException**.</span><span class="sxs-lookup"><span data-stu-id="da4f0-112">Instead, the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event handler receives an [**IAnalysisStatus**](ianalysisstatus.md) that contains an [**IAnalysisWarning**](ianalysiswarning.md) with an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) of **AnalysisWarningCode\_BackgroundException**.</span></span> <span data-ttu-id="da4f0-113">Este **IAnalysisWarning** contiene el código de error de la operación de análisis en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="da4f0-113">This **IAnalysisWarning** contains the error code for the background analysis operation.</span></span> <span data-ttu-id="da4f0-114">En general, el controlador de eventos **\_ IAnalysisEvents:: Results** devolverá este código de error para que se pueda administrar en cualquier parte de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="da4f0-114">In general, your **\_IAnalysisEvents::Results** event handler will return this error code so that it can be handled elsewhere in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="da4f0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da4f0-115">Requirements</span></span>



| <span data-ttu-id="da4f0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="da4f0-116">Requirement</span></span> | <span data-ttu-id="da4f0-117">Value</span><span class="sxs-lookup"><span data-stu-id="da4f0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da4f0-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da4f0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="da4f0-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="da4f0-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="da4f0-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da4f0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="da4f0-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="da4f0-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="da4f0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da4f0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="da4f0-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="da4f0-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="da4f0-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="da4f0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da4f0-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da4f0-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="da4f0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="da4f0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4f0-127">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="da4f0-127">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="da4f0-128">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="da4f0-128">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="da4f0-129">**IInkAnalyzer:: BackgroundAnalyze (método)**</span><span class="sxs-lookup"><span data-stu-id="da4f0-129">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="da4f0-130">**\_IAnalysisEvents:: results**</span><span class="sxs-lookup"><span data-stu-id="da4f0-130">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="da4f0-131">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="da4f0-131">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="da4f0-132">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="da4f0-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

