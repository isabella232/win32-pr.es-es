---
description: Crea un nuevo nodo de reconocedor personalizado para el IInkAnalyzer.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'IInkAnalyzer:: CreateCustomRecognizer (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 70cc5741faa8d54d09af000d4dbbb3c0fc423df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275471"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a><span data-ttu-id="e3dcf-103">IInkAnalyzer:: CreateCustomRecognizer (método)</span><span class="sxs-lookup"><span data-stu-id="e3dcf-103">IInkAnalyzer::CreateCustomRecognizer method</span></span>

<span data-ttu-id="e3dcf-104">Crea un nuevo nodo de reconocedor personalizado para el [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="e3dcf-104">Creates a new custom recognizer node for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3dcf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3dcf-105">Syntax</span></span>


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="e3dcf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3dcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3dcf-107">*pInkAnalysisRecognizerId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3dcf-107">*pInkAnalysisRecognizerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3dcf-108">Identificador único global (GUID) del [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) para el que se va a crear un nodo.</span><span class="sxs-lookup"><span data-stu-id="e3dcf-108">The globally unique identifier (GUID) of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) for which to create a node.</span></span>

</dd> <dt>

<span data-ttu-id="e3dcf-109">*ppContextNode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e3dcf-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3dcf-110">Un puntero al objeto [**IContextNode**](icontextnode.md) que representa el nuevo nodo de reconocedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="e3dcf-110">A pointer to the [**IContextNode**](icontextnode.md) object representing the new custom recognizer node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3dcf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3dcf-111">Return value</span></span>

<span data-ttu-id="e3dcf-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e3dcf-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e3dcf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3dcf-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e3dcf-114">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en ppContextNode cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="e3dcf-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on ppContextNode when you no longer need to use the object.</span></span>

 

<span data-ttu-id="e3dcf-115">Este método crea un nuevo [**IContextNode**](icontextnode.md) con un tipo de CustomRecognizer (vea [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="e3dcf-115">This method creates a new [**IContextNode**](icontextnode.md) with a type of CustomRecognizer (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="e3dcf-116">A continuación, agrega el nuevo nodo de reconocedor personalizado a la colección de subnodos del nodo raíz del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) y [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="e3dcf-116">It then adds the new custom recognizer node to the subnodes collection of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3dcf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3dcf-117">Requirements</span></span>



| <span data-ttu-id="e3dcf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3dcf-118">Requirement</span></span> | <span data-ttu-id="e3dcf-119">Value</span><span class="sxs-lookup"><span data-stu-id="e3dcf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3dcf-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3dcf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3dcf-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e3dcf-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e3dcf-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3dcf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3dcf-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e3dcf-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e3dcf-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3dcf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3dcf-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e3dcf-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e3dcf-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e3dcf-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3dcf-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3dcf-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e3dcf-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3dcf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3dcf-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e3dcf-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e3dcf-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="e3dcf-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e3dcf-131">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="e3dcf-131">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="e3dcf-132">**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (método)**</span><span class="sxs-lookup"><span data-stu-id="e3dcf-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="e3dcf-133">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="e3dcf-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

