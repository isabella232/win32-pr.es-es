---
description: Recupera una matriz de identificadores para los trazos dentro del objeto IContextNode.
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: 'IContextNode:: GetStrokeIds (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 25592cd245eba135fa7e459ff3c5c5207fc6ff0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154437"
---
# <a name="icontextnodegetstrokeids-method"></a><span data-ttu-id="8de95-103">IContextNode:: GetStrokeIds (método)</span><span class="sxs-lookup"><span data-stu-id="8de95-103">IContextNode::GetStrokeIds method</span></span>

<span data-ttu-id="8de95-104">Recupera una matriz de identificadores para los trazos dentro del objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="8de95-104">Retrieves an array of identifiers for the strokes within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8de95-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8de95-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="8de95-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8de95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8de95-107">*pulStrokeIdsCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8de95-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8de95-108">Número de trazos.</span><span class="sxs-lookup"><span data-stu-id="8de95-108">The number of strokes.</span></span> <span data-ttu-id="8de95-109">No se utiliza el valor que se pasa.</span><span class="sxs-lookup"><span data-stu-id="8de95-109">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8de95-110">*pplStrokes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8de95-110">*pplStrokes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8de95-111">Puntero a la matriz de identificadores de trazo para este objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="8de95-111">A pointer to the array of stroke identifiers for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8de95-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8de95-112">Return value</span></span>

<span data-ttu-id="8de95-113">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8de95-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8de95-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8de95-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8de95-115">Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *pplStrokes* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="8de95-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokes* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8de95-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8de95-116">Requirements</span></span>



| <span data-ttu-id="8de95-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8de95-117">Requirement</span></span> | <span data-ttu-id="8de95-118">Value</span><span class="sxs-lookup"><span data-stu-id="8de95-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8de95-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8de95-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8de95-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8de95-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8de95-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8de95-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8de95-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8de95-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8de95-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8de95-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8de95-124"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8de95-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8de95-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8de95-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8de95-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8de95-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8de95-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8de95-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de95-128">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="8de95-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="8de95-129">**IContextNode::GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="8de95-129">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="8de95-130">**IContextNode::GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="8de95-130">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="8de95-131">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="8de95-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

