---
description: Recupera el IInkAnalysisRecognizer en el índice especificado.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'IInkAnalysisRecognizers:: GetInkAnalysisRecognizer (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1008ae0b26d30233c3b00167391523d321cd381e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497572"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a><span data-ttu-id="af83e-103">IInkAnalysisRecognizers:: GetInkAnalysisRecognizer (método)</span><span class="sxs-lookup"><span data-stu-id="af83e-103">IInkAnalysisRecognizers::GetInkAnalysisRecognizer method</span></span>

<span data-ttu-id="af83e-104">Recupera el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="af83e-104">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="af83e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af83e-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="af83e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af83e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af83e-107">*ulIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af83e-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af83e-108">Índice de base cero del objeto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="af83e-108">The zero-based index of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="af83e-109">*ppInkAnalysisRecognizer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="af83e-109">*ppInkAnalysisRecognizer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af83e-110">Puntero a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="af83e-110">A pointer to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af83e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af83e-111">Return value</span></span>

<span data-ttu-id="af83e-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="af83e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="af83e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af83e-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="af83e-114">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppInkAnalysisRecognizer* cuando ya no necesite usar el reconocedor de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="af83e-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppInkAnalysisRecognizer* when you no longer need to use the ink analysis recognizer.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="af83e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af83e-115">Requirements</span></span>



| <span data-ttu-id="af83e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="af83e-116">Requirement</span></span> | <span data-ttu-id="af83e-117">Value</span><span class="sxs-lookup"><span data-stu-id="af83e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af83e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af83e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af83e-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="af83e-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="af83e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af83e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af83e-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="af83e-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="af83e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af83e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="af83e-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="af83e-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="af83e-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="af83e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af83e-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af83e-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="af83e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="af83e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af83e-127">**InkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="af83e-127">**InkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="af83e-128">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="af83e-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

