---
description: Recupera el objeto IContextNode que es el destino de este IContextLink.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'IContextLink:: GetDestinationNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360344"
---
# <a name="icontextlinkgetdestinationnode-method"></a><span data-ttu-id="5d338-103">IContextLink:: GetDestinationNode (método)</span><span class="sxs-lookup"><span data-stu-id="5d338-103">IContextLink::GetDestinationNode method</span></span>

<span data-ttu-id="5d338-104">Recupera el objeto [**IContextNode**](icontextnode.md) que es el destino de este [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="5d338-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d338-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d338-105">Syntax</span></span>


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="5d338-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d338-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d338-107">*ppDstContextNodeId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5d338-107">*ppDstContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d338-108">Un puntero al objeto [**IContextNode**](icontextnode.md) que es el destino de este [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="5d338-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d338-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d338-109">Return value</span></span>

<span data-ttu-id="5d338-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5d338-110">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d338-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d338-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="5d338-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppDstContextNodeId* cuando ya no necesite usar el nodo de destino.</span><span class="sxs-lookup"><span data-stu-id="5d338-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppDstContextNodeId* when you no longer need to use the destination node.</span></span>

 

<span data-ttu-id="5d338-113">Si el objeto [**IContextLink**](icontextlink.md) se vincula entre un nodo que contiene escritura y un nodo que contiene dibujos, el nodo de destino es generalmente el nodo que contiene la escritura.</span><span class="sxs-lookup"><span data-stu-id="5d338-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the destination node is generally the node that contains writing.</span></span>

<span data-ttu-id="5d338-114">Si el objeto [**IContextLink**](icontextlink.md) tiene un tipo de vínculo de encloses (vea [**IContextLink:: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), el nodo de destino es el objeto [**IContextNode**](icontextnode.md) que se incluye.</span><span class="sxs-lookup"><span data-stu-id="5d338-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the destination node is the [**IContextNode**](icontextnode.md) object that is enclosed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d338-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d338-115">Requirements</span></span>



| <span data-ttu-id="5d338-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d338-116">Requirement</span></span> | <span data-ttu-id="5d338-117">Value</span><span class="sxs-lookup"><span data-stu-id="5d338-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d338-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d338-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5d338-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5d338-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5d338-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d338-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5d338-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5d338-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5d338-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d338-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d338-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5d338-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5d338-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d338-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d338-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d338-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5d338-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d338-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d338-127">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="5d338-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="5d338-128">**IContextLink::GetSourceNode**</span><span class="sxs-lookup"><span data-stu-id="5d338-128">**IContextLink::GetSourceNode**</span></span>](icontextlink-getsourcenode.md)
</dt> <dt>

[<span data-ttu-id="5d338-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="5d338-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="5d338-130">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="5d338-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

