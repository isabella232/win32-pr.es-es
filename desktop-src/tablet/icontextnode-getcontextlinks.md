---
description: Recupera una colección de objetos IContextLink que representa relaciones con otros objetos IContextNode.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'IContextNode:: GetContextLinks (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de62550a09d0a538ddc680f6d57c35a1016fe255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652435"
---
# <a name="icontextnodegetcontextlinks-method"></a><span data-ttu-id="14e83-103">IContextNode:: GetContextLinks (método)</span><span class="sxs-lookup"><span data-stu-id="14e83-103">IContextNode::GetContextLinks method</span></span>

<span data-ttu-id="14e83-104">Recupera una colección de objetos [**IContextLink**](icontextlink.md) que representa relaciones con otros objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="14e83-104">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e83-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14e83-105">Syntax</span></span>


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a><span data-ttu-id="14e83-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14e83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14e83-107">*ppContextLinks* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="14e83-107">*ppContextLinks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14e83-108">Puntero a una colección de objetos [**IContextLink**](icontextlink.md) que representa relaciones con otros objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="14e83-108">A pointer to a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14e83-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14e83-109">Return value</span></span>

<span data-ttu-id="14e83-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="14e83-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="14e83-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14e83-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="14e83-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextLinks* cuando ya no necesite usar la colección de vínculos de contexto.</span><span class="sxs-lookup"><span data-stu-id="14e83-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinks* when you no longer need to use the context links collection.</span></span>

 

<span data-ttu-id="14e83-113">Para obtener información sobre las relaciones entre los nodos primarios y secundarios, use [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) o [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md).</span><span class="sxs-lookup"><span data-stu-id="14e83-113">To get information about parent or child node relationships, use [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) or [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md).</span></span>

<span data-ttu-id="14e83-114">Para obtener más información sobre los tipos de relaciones que se describen en los vínculos, vea [**IContextLink**](icontextlink.md) y [**ContextLinkDirection**](contextlinkdirection.md).</span><span class="sxs-lookup"><span data-stu-id="14e83-114">For more information about the kinds of relationships that are described by links, see [**IContextLink**](icontextlink.md) and [**ContextLinkDirection**](contextlinkdirection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14e83-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14e83-115">Requirements</span></span>



| <span data-ttu-id="14e83-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="14e83-116">Requirement</span></span> | <span data-ttu-id="14e83-117">Value</span><span class="sxs-lookup"><span data-stu-id="14e83-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14e83-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14e83-118">Minimum supported client</span></span><br/> | <span data-ttu-id="14e83-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="14e83-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="14e83-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14e83-120">Minimum supported server</span></span><br/> | <span data-ttu-id="14e83-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="14e83-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="14e83-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14e83-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="14e83-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="14e83-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="14e83-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="14e83-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14e83-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14e83-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="14e83-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="14e83-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e83-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="14e83-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="14e83-128">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="14e83-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="14e83-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="14e83-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="14e83-130">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="14e83-130">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="14e83-131">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="14e83-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

