---
description: Comprueba si BoundingBox contiene un objeto especificado.
ms.assetid: 876c7764-9378-48e5-812c-3646930900c5
title: BoundingBox. Contains (métodos)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 485dbbaf5ab4522eb50fe598325e5ecbb48fff57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544187"
---
# <a name="boundingboxcontains-methods"></a><span data-ttu-id="c2185-103">BoundingBox. Contains (métodos)</span><span class="sxs-lookup"><span data-stu-id="c2185-103">BoundingBox.Contains methods</span></span>

<span data-ttu-id="c2185-104">Comprueba si BoundingBox contiene un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="c2185-104">Tests whether the BoundingBox contains a specified object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="c2185-105">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="c2185-105">Overload list</span></span>



| <span data-ttu-id="c2185-106">Método</span><span class="sxs-lookup"><span data-stu-id="c2185-106">Method</span></span>                                                                               | <span data-ttu-id="c2185-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2185-107">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2185-108">**BoundingBox:: Contains (XMVECTOR)**</span><span class="sxs-lookup"><span data-stu-id="c2185-108">**BoundingBox::Contains (XMVECTOR)**</span></span>](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains)                   | <span data-ttu-id="c2185-109">Comprueba si el BoundingBox contiene un punto especificado.</span><span class="sxs-lookup"><span data-stu-id="c2185-109">Tests the whether the BoundingBox contains a specified point.</span></span><br/>                                                                   |
| <span data-ttu-id="c2185-110">[**BoundingBox:: Contains (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="c2185-110">[**BoundingBox::Contains (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingbox_))</span></span>         | <span data-ttu-id="c2185-111">Comprueba si el BoundingBox contiene otro BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="c2185-111">Tests whether the BoundingBox contains another BoundingBox.</span></span><br/>                                                                     |
| <span data-ttu-id="c2185-112">[**BoundingBox:: Contains (const BoundingSphere&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingsphere_))</span><span class="sxs-lookup"><span data-stu-id="c2185-112">[**BoundingBox::Contains (const BoundingSphere&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingsphere_))</span></span>      | <span data-ttu-id="c2185-113">Comprueba si BoundingBox contiene un BoundingSphere especificado.</span><span class="sxs-lookup"><span data-stu-id="c2185-113">Tests whether the BoundingBox contains a specified BoundingSphere.</span></span><br/>                                                              |
| <span data-ttu-id="c2185-114">[**BoundingBox:: Contains (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="c2185-114">[**BoundingBox::Contains (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingfrustum_))</span></span>     | <span data-ttu-id="c2185-115">Comprueba si [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) contiene el [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum)especificado.</span><span class="sxs-lookup"><span data-stu-id="c2185-115">Tests whether the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) contains the specified [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span></span><br/>         |
| <span data-ttu-id="c2185-116">[**BoundingBox:: Contains (XMVECTOR, XMVECTOR, XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="c2185-116">[**BoundingBox::Contains (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="c2185-117">Comprueba si el BoundingBox contiene un triángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="c2185-117">Test whether the BoundingBox contains a specified triangle.</span></span><br/>                                                                     |
| <span data-ttu-id="c2185-118">[**BoundingBox:: Contains (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="c2185-118">[**BoundingBox::Contains (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-contains(constboundingorientedbox_))</span></span> | <span data-ttu-id="c2185-119">Comprueba si [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) contiene el [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox)especificado.</span><span class="sxs-lookup"><span data-stu-id="c2185-119">Tests whether the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) contains the specified [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2185-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2185-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2185-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2185-121">Methods</span></span>](boundingbox-methods.md)
</dt> <dt>

<span data-ttu-id="c2185-122">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c2185-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c2185-123">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="c2185-123">**BoundingBox**</span></span>](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)
</dt> </dl>

 

 
