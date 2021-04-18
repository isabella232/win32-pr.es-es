---
description: Obtiene los objetos IContextNode asociados a esta alternativa.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'IAnalysisAlternate:: GetAlternateNodes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: dd24581774c2115c9f7ccb6857d0cd4d9e1bfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686834"
---
# <a name="ianalysisalternategetalternatenodes-method"></a><span data-ttu-id="91c24-103">IAnalysisAlternate:: GetAlternateNodes (método)</span><span class="sxs-lookup"><span data-stu-id="91c24-103">IAnalysisAlternate::GetAlternateNodes method</span></span>

<span data-ttu-id="91c24-104">Obtiene los objetos [**IContextNode**](icontextnode.md) asociados a esta alternativa.</span><span class="sxs-lookup"><span data-stu-id="91c24-104">Gets the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c24-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91c24-105">Syntax</span></span>


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a><span data-ttu-id="91c24-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91c24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91c24-107">*ppAlternateNodes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="91c24-107">*ppAlternateNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91c24-108">Un puntero a la colección [**IContextNodes**](icontextnodes.md) que contiene objetos [**IContextNode**](icontextnode.md) que están asociados a esta alternativa.</span><span class="sxs-lookup"><span data-stu-id="91c24-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection that contains [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91c24-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91c24-109">Return value</span></span>

<span data-ttu-id="91c24-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="91c24-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="91c24-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91c24-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="91c24-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppAlternateNodes* cuando ya no necesite usar la colección de nodos de contexto.</span><span class="sxs-lookup"><span data-stu-id="91c24-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternateNodes* when you no longer need to use the context node collection.</span></span>

 

<span data-ttu-id="91c24-113">Este método devuelve los nodos de contexto hoja que están asociados a esta alternativa.</span><span class="sxs-lookup"><span data-stu-id="91c24-113">This method returns the leaf context nodes that are associated with this alternate.</span></span> <span data-ttu-id="91c24-114">Ejemplos de nodos hoja son los nodos de contexto InkWord, TextWord, Image, InkDrawing y InkBullet.</span><span class="sxs-lookup"><span data-stu-id="91c24-114">Examples of leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet context nodes.</span></span> <span data-ttu-id="91c24-115">Para obtener más información, vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [tipos de nodo de contexto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="91c24-115">For more information, see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="91c24-116">Dado que se corresponden con alternativas, estos [**objetos IContextNode**](icontextnode.md) no son descendientes del **IContextNode** raíz del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea el [**método IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)) a menos que sean la alternativa superior, que es el primer elemento de una colección [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="91c24-116">Because they correspond to alternates, these [**IContextNode**](icontextnode.md) objects are not descendants of the [**IInkAnalyzer**](iinkanalyzer.md) object's root **IContextNode** (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)) unless they are the top alternate, which is the first element in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="91c24-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91c24-117">Requirements</span></span>



| <span data-ttu-id="91c24-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="91c24-118">Requirement</span></span> | <span data-ttu-id="91c24-119">Value</span><span class="sxs-lookup"><span data-stu-id="91c24-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c24-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91c24-120">Minimum supported client</span></span><br/> | <span data-ttu-id="91c24-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="91c24-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="91c24-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91c24-122">Minimum supported server</span></span><br/> | <span data-ttu-id="91c24-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="91c24-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="91c24-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91c24-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="91c24-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="91c24-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="91c24-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="91c24-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91c24-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91c24-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="91c24-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="91c24-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c24-129">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="91c24-129">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="91c24-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="91c24-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="91c24-131">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="91c24-131">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="91c24-132">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="91c24-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> <dt>

[<span data-ttu-id="91c24-133">System. Windows. Ink. AnalysisCore. AnalysisAlternateBase. AlternateNodes</span><span class="sxs-lookup"><span data-stu-id="91c24-133">System.Windows.Ink.AnalysisCore.AnalysisAlternateBase.AlternateNodes</span></span>](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

