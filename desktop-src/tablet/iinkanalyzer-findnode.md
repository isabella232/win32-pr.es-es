---
description: Recupera el objeto IContextNode para un identificador único global (GUID) especificado.
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: 'IInkAnalyzer:: FindNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 66771678253f1724653d87ad9c54d474a9ceceb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082151"
---
# <a name="iinkanalyzerfindnode-method"></a><span data-ttu-id="b8bb9-103">IInkAnalyzer:: FindNode (método)</span><span class="sxs-lookup"><span data-stu-id="b8bb9-103">IInkAnalyzer::FindNode method</span></span>

<span data-ttu-id="b8bb9-104">Recupera el objeto [**IContextNode**](icontextnode.md) para un identificador único global (GUID) especificado.</span><span class="sxs-lookup"><span data-stu-id="b8bb9-104">Retrieves the [**IContextNode**](icontextnode.md) object for a specified globally unique identifier (GUID).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8bb9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8bb9-105">Syntax</span></span>


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a><span data-ttu-id="b8bb9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8bb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8bb9-107">*pId* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b8bb9-107">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8bb9-108">Identificador del objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b8bb9-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="b8bb9-109">*ppContextNodeFound* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b8bb9-109">*ppContextNodeFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8bb9-110">Un puntero al objeto [**IContextNode**](icontextnode.md) con el identificador de *pId* .</span><span class="sxs-lookup"><span data-stu-id="b8bb9-110">A pointer to the [**IContextNode**](icontextnode.md) object with the *pId* identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8bb9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8bb9-111">Return value</span></span>

<span data-ttu-id="b8bb9-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b8bb9-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8bb9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8bb9-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b8bb9-114">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeFound* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="b8bb9-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="b8bb9-115">Si no existe ningún objeto [**IContextNode**](icontextnode.md) como descendiente del nodo raíz [**IInkAnalyzer**](iinkanalyzer.md) , se devuelve **null** .</span><span class="sxs-lookup"><span data-stu-id="b8bb9-115">If no such [**IContextNode**](icontextnode.md) object exists as a descendant of the [**IInkAnalyzer**](iinkanalyzer.md) root node, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8bb9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8bb9-116">Requirements</span></span>



| <span data-ttu-id="b8bb9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8bb9-117">Requirement</span></span> | <span data-ttu-id="b8bb9-118">Value</span><span class="sxs-lookup"><span data-stu-id="b8bb9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8bb9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8bb9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b8bb9-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b8bb9-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b8bb9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8bb9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b8bb9-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b8bb9-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b8bb9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8bb9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8bb9-124"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b8bb9-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b8bb9-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8bb9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8bb9-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8bb9-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b8bb9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8bb9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8bb9-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b8bb9-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b8bb9-129">**IInkAnalyzer:: FindInkLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="b8bb9-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="b8bb9-130">**IInkAnalyzer:: FindInkLeafNodesForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="b8bb9-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="b8bb9-131">**IInkAnalyzer:: FindLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="b8bb9-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="b8bb9-132">**IInkAnalyzer:: FindNodesOfType (método)**</span><span class="sxs-lookup"><span data-stu-id="b8bb9-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="b8bb9-133">**IInkAnalyzer:: FindNodesOfTypeForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="b8bb9-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="b8bb9-134">**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="b8bb9-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="b8bb9-135">**IInkAnalyzer:: FindNodesWithCallBack (método)**</span><span class="sxs-lookup"><span data-stu-id="b8bb9-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="b8bb9-136">**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="b8bb9-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="b8bb9-137">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="b8bb9-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

