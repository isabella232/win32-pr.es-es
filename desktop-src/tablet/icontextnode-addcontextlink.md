---
description: Agrega un nuevo IContextLink a la colección del objeto IContextNode de vínculos de contexto.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'IContextNode:: AddContextLink (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eccfcc8be51ff951c1bcd6de55bd3a0f89cdc201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652438"
---
# <a name="icontextnodeaddcontextlink-method"></a><span data-ttu-id="43dd0-103">IContextNode:: AddContextLink (método)</span><span class="sxs-lookup"><span data-stu-id="43dd0-103">IContextNode::AddContextLink method</span></span>

<span data-ttu-id="43dd0-104">Agrega un nuevo [**IContextLink**](icontextlink.md) a la colección del objeto [**IContextNode**](icontextnode.md) de vínculos de contexto.</span><span class="sxs-lookup"><span data-stu-id="43dd0-104">Adds a new [**IContextLink**](icontextlink.md) to the [**IContextNode**](icontextnode.md) object's collection of context links.</span></span>

## <a name="syntax"></a><span data-ttu-id="43dd0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43dd0-105">Syntax</span></span>


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a><span data-ttu-id="43dd0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43dd0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43dd0-107">*pDestinationNode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43dd0-107">*pDestinationNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43dd0-108">[**IContextNode**](icontextnode.md) de destino para el nuevo [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="43dd0-108">The destination [**IContextNode**](icontextnode.md) for the new [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="43dd0-109">*linkDirection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43dd0-109">*linkDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43dd0-110">Dirección del objeto [**IContextLink**](icontextlink.md) que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="43dd0-110">The direction of [**IContextLink**](icontextlink.md) object to create.</span></span>

</dd> <dt>

<span data-ttu-id="43dd0-111">*ppContextLinkToAdd* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="43dd0-111">*ppContextLinkToAdd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43dd0-112">Puntero al nuevo objeto [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="43dd0-112">A pointer to the new [**IContextLink**](icontextlink.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43dd0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43dd0-113">Return value</span></span>

<span data-ttu-id="43dd0-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="43dd0-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="43dd0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43dd0-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="43dd0-116">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextLinkToAdd* cuando ya no necesite usar el nodo de contexto.</span><span class="sxs-lookup"><span data-stu-id="43dd0-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinkToAdd* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="43dd0-117">Este objeto [**IContextNode**](icontextnode.md) es el nodo de origen (vea [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md)) para el nuevo objeto [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="43dd0-117">This [**IContextNode**](icontextnode.md) object is the source node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)) for the new [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="43dd0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43dd0-118">Requirements</span></span>



| <span data-ttu-id="43dd0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="43dd0-119">Requirement</span></span> | <span data-ttu-id="43dd0-120">Value</span><span class="sxs-lookup"><span data-stu-id="43dd0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43dd0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43dd0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="43dd0-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="43dd0-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="43dd0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43dd0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="43dd0-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="43dd0-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="43dd0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43dd0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="43dd0-126"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="43dd0-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="43dd0-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="43dd0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43dd0-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43dd0-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="43dd0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="43dd0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43dd0-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="43dd0-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="43dd0-131">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="43dd0-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="43dd0-132">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="43dd0-132">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="43dd0-133">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="43dd0-133">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="43dd0-134">**IContextNode::D eleteContextLink**</span><span class="sxs-lookup"><span data-stu-id="43dd0-134">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="43dd0-135">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="43dd0-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="43dd0-136">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="43dd0-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

