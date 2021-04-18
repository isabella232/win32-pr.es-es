---
description: Elimina un objeto IContextLink de la colección de vínculos del objeto IContextNode.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: IContextNode::D método eleteContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac5676635bec961129078ed8689169d1a81cd87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715231"
---
# <a name="icontextnodedeletecontextlink-method"></a><span data-ttu-id="fb4fe-103">IContextNode::D método eleteContextLink</span><span class="sxs-lookup"><span data-stu-id="fb4fe-103">IContextNode::DeleteContextLink method</span></span>

<span data-ttu-id="fb4fe-104">Elimina un objeto [**IContextLink**](icontextlink.md) de la colección de vínculos del objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="fb4fe-104">Deletes an [**IContextLink**](icontextlink.md) object from the [**IContextNode**](icontextnode.md) object's link collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb4fe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb4fe-105">Syntax</span></span>


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="fb4fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb4fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb4fe-107">*pContextLinkToDelete* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb4fe-107">*pContextLinkToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb4fe-108">Objeto [**IContextLink**](icontextlink.md) que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="fb4fe-108">The [**IContextLink**](icontextlink.md) object to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb4fe-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb4fe-109">Return value</span></span>

<span data-ttu-id="fb4fe-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fb4fe-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb4fe-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb4fe-111">Remarks</span></span>

<span data-ttu-id="fb4fe-112">Un vínculo de contexto tiene un nodo de origen y un nodo de destino (vea [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md) y [**IContextLink:: GetDestinationNode**](icontextlink-getdestinationnode.md)).</span><span class="sxs-lookup"><span data-stu-id="fb4fe-112">A context link has a source node and a destination node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span> <span data-ttu-id="fb4fe-113">Este método quita el [**IContextLink**](icontextlink.md) de la colección de los nodos de origen y de destino de los vínculos de contexto (vea [**IContextNode:: GetContextLinks**](icontextnode-getcontextlinks.md)).</span><span class="sxs-lookup"><span data-stu-id="fb4fe-113">This method removes the [**IContextLink**](icontextlink.md) from both the source and destination nodes' collection of context links (see [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb4fe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb4fe-114">Requirements</span></span>



| <span data-ttu-id="fb4fe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb4fe-115">Requirement</span></span> | <span data-ttu-id="fb4fe-116">Value</span><span class="sxs-lookup"><span data-stu-id="fb4fe-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4fe-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb4fe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fb4fe-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fb4fe-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fb4fe-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb4fe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fb4fe-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fb4fe-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fb4fe-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb4fe-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb4fe-122"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fb4fe-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fb4fe-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb4fe-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb4fe-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb4fe-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fb4fe-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb4fe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb4fe-126">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="fb4fe-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="fb4fe-127">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="fb4fe-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="fb4fe-128">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="fb4fe-128">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="fb4fe-129">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="fb4fe-129">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="fb4fe-130">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="fb4fe-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




