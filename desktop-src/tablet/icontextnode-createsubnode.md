---
description: Crea un nuevo objeto IContextNode secundario.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'IContextNode:: CreateSubNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 02c10cc50b90b96cc1ce4aadfa97f86a6c516ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908026"
---
# <a name="icontextnodecreatesubnode-method"></a><span data-ttu-id="0e9fc-103">IContextNode:: CreateSubNode (método)</span><span class="sxs-lookup"><span data-stu-id="0e9fc-103">IContextNode::CreateSubNode method</span></span>

<span data-ttu-id="0e9fc-104">Crea un nuevo objeto [**IContextNode**](icontextnode.md) secundario.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-104">Creates a new child [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9fc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e9fc-105">Syntax</span></span>


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="0e9fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e9fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e9fc-107">*pNodeType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0e9fc-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9fc-108">**GUID** que representa el tipo de [**IContextNode**](icontextnode.md) que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-108">A **GUID** that represents the type of [**IContextNode**](icontextnode.md) to create.</span></span>

</dd> <dt>

<span data-ttu-id="0e9fc-109">*ppContextNodeCreated* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0e9fc-109">*ppContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9fc-110">Puntero al nuevo [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="0e9fc-110">A pointer to the new [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e9fc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e9fc-111">Return value</span></span>

<span data-ttu-id="0e9fc-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0e9fc-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e9fc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e9fc-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="0e9fc-114">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextNodeCreated* cuando ya no necesite usar el nodo de contexto.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="0e9fc-115">El nuevo [**IContextNode**](icontextnode.md) se agrega a la colección de nodos secundarios del nodo de contexto (vea [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="0e9fc-115">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="0e9fc-116">Cuando hay nodos secundarios existentes, el **IContextNode** recién creado se agrega como el último nodo secundario.</span><span class="sxs-lookup"><span data-stu-id="0e9fc-116">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="0e9fc-117">Para obtener una lista de tipos de nodo de contexto, consulte [tipos de nodo de contexto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="0e9fc-117">For a list of context node types, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e9fc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e9fc-118">Requirements</span></span>



| <span data-ttu-id="0e9fc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e9fc-119">Requirement</span></span> | <span data-ttu-id="0e9fc-120">Value</span><span class="sxs-lookup"><span data-stu-id="0e9fc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e9fc-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e9fc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e9fc-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0e9fc-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0e9fc-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e9fc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e9fc-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0e9fc-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0e9fc-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e9fc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e9fc-126"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0e9fc-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0e9fc-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0e9fc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e9fc-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e9fc-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0e9fc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e9fc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e9fc-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="0e9fc-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="0e9fc-131">**IContextNode::D eleteSubNode**</span><span class="sxs-lookup"><span data-stu-id="0e9fc-131">**IContextNode::DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)
</dt> <dt>

[<span data-ttu-id="0e9fc-132">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="0e9fc-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

