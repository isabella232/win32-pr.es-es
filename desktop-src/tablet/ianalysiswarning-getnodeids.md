---
description: Devuelve los identificadores de los nodos de contexto pertinentes que están asociados a esta advertencia.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'IAnalysisWarning:: GetNodeIds (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542078"
---
# <a name="ianalysiswarninggetnodeids-method"></a><span data-ttu-id="5cd92-103">IAnalysisWarning:: GetNodeIds (método)</span><span class="sxs-lookup"><span data-stu-id="5cd92-103">IAnalysisWarning::GetNodeIds method</span></span>

<span data-ttu-id="5cd92-104">Devuelve los identificadores de los nodos de contexto pertinentes que están asociados a esta advertencia.</span><span class="sxs-lookup"><span data-stu-id="5cd92-104">Returns the identifiers of any relevant context nodes that are associated with this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cd92-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5cd92-105">Syntax</span></span>


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a><span data-ttu-id="5cd92-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5cd92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cd92-107">*pulCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5cd92-107">*pulCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5cd92-108">El número de identificadores únicos globales (GUID) en *ppNodeIds*.</span><span class="sxs-lookup"><span data-stu-id="5cd92-108">The number of globally unique identifiers (GUIDs) in *ppNodeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="5cd92-109">*ppNodeIds* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5cd92-109">*ppNodeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5cd92-110">Puntero a una matriz de GUID que identifica los nodos de contexto asociados a esta advertencia de análisis, o **null** si no hay ningún nodo de contexto asociado a la advertencia.</span><span class="sxs-lookup"><span data-stu-id="5cd92-110">A pointer to an array of GUIDs that identifies the context nodes that are associated with this analysis warning, or **NULL** if no context nodes are associated with the warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cd92-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5cd92-111">Return value</span></span>

<span data-ttu-id="5cd92-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5cd92-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5cd92-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cd92-113">Remarks</span></span>

<span data-ttu-id="5cd92-114">Si *ppNodeIds* se pasa como **null**, el método **GetNodeIds** devuelve **S \_ correcto** y el número de rectángulos se devuelve en *pulCount*.</span><span class="sxs-lookup"><span data-stu-id="5cd92-114">If *ppNodeIds* is passed as **NULL**, the **GetNodeIds** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="5cd92-115">Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppNodeIds* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="5cd92-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppNodeIds* when you no longer need the information.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5cd92-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5cd92-116">Examples</span></span>

<span data-ttu-id="5cd92-117">En el ejemplo siguiente se muestra cómo obtener los objetos [**IContextNode**](icontextnode.md) que se encuentran en [**IAnalysisWarning**](ianalysiswarning.md), `warning` y cómo obtener solo el número de objetos **IContextNode**</span><span class="sxs-lookup"><span data-stu-id="5cd92-117">The following example shows how to get the [**IContextNode**](icontextnode.md) objects that are in the [**IAnalysisWarning**](ianalysiswarning.md), `warning`, and how to get only the number of **IContextNode** objects</span></span>


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="5cd92-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cd92-118">Requirements</span></span>



| <span data-ttu-id="5cd92-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cd92-119">Requirement</span></span> | <span data-ttu-id="5cd92-120">Value</span><span class="sxs-lookup"><span data-stu-id="5cd92-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cd92-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cd92-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5cd92-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5cd92-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5cd92-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cd92-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5cd92-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5cd92-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5cd92-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cd92-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cd92-126"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5cd92-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5cd92-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5cd92-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cd92-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cd92-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5cd92-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5cd92-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cd92-130">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="5cd92-130">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="5cd92-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="5cd92-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="5cd92-132">**IInkAnalyzer:: FindNode (método)**</span><span class="sxs-lookup"><span data-stu-id="5cd92-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="5cd92-133">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="5cd92-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

