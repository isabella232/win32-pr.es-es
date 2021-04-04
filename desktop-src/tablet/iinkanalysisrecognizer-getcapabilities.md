---
description: Recupera las capacidades del reconocedor.
ms.assetid: 9014bd9b-54fb-4735-9eb8-56a6188a5fc0
title: 'IInkAnalysisRecognizer:: GetCapabilities (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetCapabilities
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07b66ffbed6f3e57edb8a6bfad36959fabbc047c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154426"
---
# <a name="iinkanalysisrecognizergetcapabilities-method"></a><span data-ttu-id="4a0f5-103">IInkAnalysisRecognizer:: GetCapabilities (método)</span><span class="sxs-lookup"><span data-stu-id="4a0f5-103">IInkAnalysisRecognizer::GetCapabilities method</span></span>

<span data-ttu-id="4a0f5-104">Recupera las capacidades del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="4a0f5-104">Retrieves the capabilities of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a0f5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a0f5-105">Syntax</span></span>


```C++
HRESULT GetCapabilities(
  [out] InkAnalysisRecognizerCapabilities *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="4a0f5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a0f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a0f5-107">*pCapabilities* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4a0f5-107">*pCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a0f5-108">Combinación bit a bit de los valores de [**RecognizerCapabilities**](recognizercapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="4a0f5-108">A bitwise combination of [**RecognizerCapabilities**](recognizercapabilities.md) values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a0f5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a0f5-109">Return value</span></span>

<span data-ttu-id="4a0f5-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4a0f5-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a0f5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a0f5-111">Remarks</span></span>

<span data-ttu-id="4a0f5-112">Este valor es constante para cada [ **IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)</span><span class="sxs-lookup"><span data-stu-id="4a0f5-112">This value is constant for each [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="4a0f5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a0f5-113">Requirements</span></span>



| <span data-ttu-id="4a0f5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a0f5-114">Requirement</span></span> | <span data-ttu-id="4a0f5-115">Value</span><span class="sxs-lookup"><span data-stu-id="4a0f5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a0f5-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a0f5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4a0f5-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4a0f5-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4a0f5-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a0f5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4a0f5-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4a0f5-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4a0f5-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a0f5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a0f5-121"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4a0f5-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4a0f5-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a0f5-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a0f5-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a0f5-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4a0f5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a0f5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a0f5-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="4a0f5-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="4a0f5-126">**RecognizerCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4a0f5-126">**RecognizerCapabilities**</span></span>](recognizercapabilities.md)
</dt> <dt>

[<span data-ttu-id="4a0f5-127">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="4a0f5-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




