---
description: Recupera el objeto IContextNode que es el origen de este IContextLink.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: 'IContextLink:: GetSourceNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eddab21740bf30c67e247cec89723bc47cd9dca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275478"
---
# <a name="icontextlinkgetsourcenode-method"></a><span data-ttu-id="dc35c-103">IContextLink:: GetSourceNode (método)</span><span class="sxs-lookup"><span data-stu-id="dc35c-103">IContextLink::GetSourceNode method</span></span>

<span data-ttu-id="dc35c-104">Recupera el objeto [**IContextNode**](icontextnode.md) que es el origen de este [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="dc35c-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc35c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc35c-105">Syntax</span></span>


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="dc35c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc35c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc35c-107">*ppSrcContextNodeId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dc35c-107">*ppSrcContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc35c-108">Un puntero al objeto [**IContextNode**](icontextnode.md) que es el origen de este [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="dc35c-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc35c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc35c-109">Return value</span></span>

<span data-ttu-id="dc35c-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dc35c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dc35c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc35c-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="dc35c-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppSrcContextNodeId* cuando ya no necesite usar el nodo de origen.</span><span class="sxs-lookup"><span data-stu-id="dc35c-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSrcContextNodeId* when you no longer need to use the source node.</span></span>

 

<span data-ttu-id="dc35c-113">Si el objeto [**IContextLink**](icontextlink.md) se vincula entre un nodo que contiene escritura y un nodo que contiene dibujos, el nodo de origen suele ser el nodo que contiene el dibujo.</span><span class="sxs-lookup"><span data-stu-id="dc35c-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the source node is generally the node that contains drawing.</span></span>

<span data-ttu-id="dc35c-114">Si el objeto [**IContextLink**](icontextlink.md) tiene un tipo de vínculo de encloses (vea [**IContextLink:: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), el nodo de origen es el nodo que incluye el nodo de destino.</span><span class="sxs-lookup"><span data-stu-id="dc35c-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the source node is the node that encloses the destination node.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc35c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc35c-115">Requirements</span></span>



| <span data-ttu-id="dc35c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc35c-116">Requirement</span></span> | <span data-ttu-id="dc35c-117">Value</span><span class="sxs-lookup"><span data-stu-id="dc35c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc35c-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc35c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dc35c-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dc35c-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dc35c-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc35c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dc35c-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dc35c-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dc35c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc35c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc35c-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dc35c-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dc35c-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc35c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc35c-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc35c-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="dc35c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc35c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc35c-127">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="dc35c-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="dc35c-128">**IContextLink::GetDestinationNode**</span><span class="sxs-lookup"><span data-stu-id="dc35c-128">**IContextLink::GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)
</dt> <dt>

[<span data-ttu-id="dc35c-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="dc35c-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="dc35c-130">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="dc35c-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

