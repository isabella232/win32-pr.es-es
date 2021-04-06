---
description: Contiene una colección de objetos que implementan la interfaz IContextLink.
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: Interfaz IContextLinks (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b68563aad471a5420b1157e1c5c12d26da17b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001190"
---
# <a name="icontextlinks-interface"></a><span data-ttu-id="acff1-103">Interfaz IContextLinks</span><span class="sxs-lookup"><span data-stu-id="acff1-103">IContextLinks interface</span></span>

<span data-ttu-id="acff1-104">Contiene una colección de objetos que implementan la interfaz [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="acff1-104">Contains a collection of objects that implement the [**IContextLink**](icontextlink.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="acff1-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="acff1-105">Members</span></span>

<span data-ttu-id="acff1-106">La interfaz **IContextLinks** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="acff1-106">The **IContextLinks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="acff1-107">**IContextLinks** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="acff1-107">**IContextLinks** also has these types of members:</span></span>

-   [<span data-ttu-id="acff1-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="acff1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="acff1-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="acff1-109">Methods</span></span>

<span data-ttu-id="acff1-110">La interfaz **IContextLinks** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="acff1-110">The **IContextLinks** interface has these methods.</span></span>



| <span data-ttu-id="acff1-111">Método</span><span class="sxs-lookup"><span data-stu-id="acff1-111">Method</span></span>                                                 | <span data-ttu-id="acff1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="acff1-112">Description</span></span>                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acff1-113">**GetContextLink**</span><span class="sxs-lookup"><span data-stu-id="acff1-113">**GetContextLink**</span></span>](icontextlinks-getcontextlink.md) | <span data-ttu-id="acff1-114">Recupera el [**IContextLink**](icontextlink.md) en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="acff1-114">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span><br/>               |
| [<span data-ttu-id="acff1-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="acff1-115">**GetCount**</span></span>](icontextlinks-getcount.md)             | <span data-ttu-id="acff1-116">Recupera el número de objetos [**IContextLink**](icontextlink.md) de esta colección.</span><span class="sxs-lookup"><span data-stu-id="acff1-116">Retrieves the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="acff1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acff1-117">Remarks</span></span>

<span data-ttu-id="acff1-118">Normalmente se tiene acceso a esta a través del método [**IContextNode:: GetContextLinks**](icontextnode-getcontextlinks.md) .</span><span class="sxs-lookup"><span data-stu-id="acff1-118">This is usually accessed through the [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="acff1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acff1-119">Requirements</span></span>



| <span data-ttu-id="acff1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="acff1-120">Requirement</span></span> | <span data-ttu-id="acff1-121">Value</span><span class="sxs-lookup"><span data-stu-id="acff1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acff1-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acff1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="acff1-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="acff1-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="acff1-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acff1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="acff1-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="acff1-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="acff1-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="acff1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="acff1-127"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="acff1-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="acff1-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="acff1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acff1-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acff1-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="acff1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="acff1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acff1-131">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="acff1-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="acff1-132">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="acff1-132">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="acff1-133">**IContextNode::D eleteContextLink**</span><span class="sxs-lookup"><span data-stu-id="acff1-133">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="acff1-134">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="acff1-134">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="acff1-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="acff1-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

