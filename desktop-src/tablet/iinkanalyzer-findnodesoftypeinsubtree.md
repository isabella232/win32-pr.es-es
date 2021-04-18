---
description: Recupera todos los objetos IContextNode del tipo especificado que son descendientes del objeto IContextNode especificado.
ms.assetid: 7e57d6ec-fe04-44c6-904f-7a212bbfcd19
title: 'IInkAnalyzer:: FindNodesOfTypeInSubTree (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 545e56d297b053b5b6f5dc61f944d6a4f6d4e03c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715207"
---
# <a name="iinkanalyzerfindnodesoftypeinsubtree-method"></a><span data-ttu-id="a554d-103">IInkAnalyzer:: FindNodesOfTypeInSubTree (método)</span><span class="sxs-lookup"><span data-stu-id="a554d-103">IInkAnalyzer::FindNodesOfTypeInSubTree method</span></span>

<span data-ttu-id="a554d-104">Recupera todos los objetos [**IContextNode**](icontextnode.md) del tipo especificado que son descendientes del objeto **IContextNode** especificado.</span><span class="sxs-lookup"><span data-stu-id="a554d-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a554d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a554d-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeInSubTree(
  [in]  const GUID          *pNodeType,
  [in]        IContextNode  *pContextNodeToSearchFrom,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="a554d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a554d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a554d-107">*pNodeType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a554d-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a554d-108">**GUID** que especifica el tipo de nodo.</span><span class="sxs-lookup"><span data-stu-id="a554d-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="a554d-109">*pContextNodeToSearchFrom* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a554d-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a554d-110">Objeto [**IContextNode**](icontextnode.md) cuyos descendientes se buscan.</span><span class="sxs-lookup"><span data-stu-id="a554d-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="a554d-111">*ppContextNodesFound* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a554d-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a554d-112">La colección [**IContextNodes**](icontextnodes.md) que contiene todos los nodos de tipo *pNodeType* que son descendientes de *pContextNodeToSearchFrom*.</span><span class="sxs-lookup"><span data-stu-id="a554d-112">The [**IContextNodes**](icontextnodes.md) collection containing all nodes of type *pNodeType* that are descendants of *pContextNodeToSearchFrom*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a554d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a554d-113">Return value</span></span>

<span data-ttu-id="a554d-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a554d-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a554d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a554d-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a554d-116">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodesFound* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="a554d-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a554d-117">Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene el nodo *pContextNodeToSearchFrom* , este método devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="a554d-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="a554d-118">La propiedad *pNodeType* debe contener un identificador único global (GUID) de las constantes de [tipos de nodo de contexto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="a554d-118">The *pNodeType* property must contain a globally unique identifier (GUID) from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="a554d-119">Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene este [**IContextNode**](icontextnode.md), se devuelve una colección [**IContextNodes**](icontextnodes.md) vacía.</span><span class="sxs-lookup"><span data-stu-id="a554d-119">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="a554d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a554d-120">Requirements</span></span>



| <span data-ttu-id="a554d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a554d-121">Requirement</span></span> | <span data-ttu-id="a554d-122">Value</span><span class="sxs-lookup"><span data-stu-id="a554d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a554d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a554d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a554d-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a554d-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a554d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a554d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a554d-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a554d-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a554d-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a554d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a554d-128"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a554d-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a554d-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a554d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a554d-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a554d-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a554d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a554d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a554d-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a554d-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a554d-133">**IInkAnalyzer:: FindInkLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="a554d-133">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="a554d-134">**IInkAnalyzer:: FindInkLeafNodesForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="a554d-134">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="a554d-135">**IInkAnalyzer:: FindLeafNodes (método)**</span><span class="sxs-lookup"><span data-stu-id="a554d-135">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="a554d-136">**IInkAnalyzer:: FindNode (método)**</span><span class="sxs-lookup"><span data-stu-id="a554d-136">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="a554d-137">**IInkAnalyzer:: FindNodesOfType (método)**</span><span class="sxs-lookup"><span data-stu-id="a554d-137">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="a554d-138">**IInkAnalyzer:: FindNodesOfTypeForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="a554d-138">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="a554d-139">**IInkAnalyzer:: FindNodesWithCallBack (método)**</span><span class="sxs-lookup"><span data-stu-id="a554d-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="a554d-140">**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="a554d-140">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="a554d-141">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="a554d-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

