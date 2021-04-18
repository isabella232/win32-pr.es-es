---
description: Contiene una colección de objetos que implementan la interfaz IContextNode y que son el resultado de una operación de análisis de tinta.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Interfaz IContextNodes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 306abcd32dcb0ee55978a6b95ee9f8a2c22cd19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715222"
---
# <a name="icontextnodes-interface"></a><span data-ttu-id="cf324-103">Interfaz IContextNodes</span><span class="sxs-lookup"><span data-stu-id="cf324-103">IContextNodes interface</span></span>

<span data-ttu-id="cf324-104">Contiene una colección de objetos que implementan la interfaz [**IContextNode**](icontextnode.md) y que son el resultado de una operación de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="cf324-104">Contains a collection of objects that implement the [**IContextNode**](icontextnode.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="cf324-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf324-105">Members</span></span>

<span data-ttu-id="cf324-106">La interfaz **IContextNodes** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cf324-106">The **IContextNodes** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cf324-107">**IContextNodes** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cf324-107">**IContextNodes** also has these types of members:</span></span>

-   [<span data-ttu-id="cf324-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf324-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cf324-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf324-109">Methods</span></span>

<span data-ttu-id="cf324-110">La interfaz **IContextNodes** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cf324-110">The **IContextNodes** interface has these methods.</span></span>



| <span data-ttu-id="cf324-111">Método</span><span class="sxs-lookup"><span data-stu-id="cf324-111">Method</span></span>                                                       | <span data-ttu-id="cf324-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf324-112">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf324-113">**AddContextNode**</span><span class="sxs-lookup"><span data-stu-id="cf324-113">**AddContextNode**</span></span>](icontextnodes-addcontextnode.md)       | <span data-ttu-id="cf324-114">Agrega un objeto [**IContextNode**](icontextnode.md) a esta colección.</span><span class="sxs-lookup"><span data-stu-id="cf324-114">Adds an [**IContextNode**](icontextnode.md) object to this collection.</span></span> <br/>                                  |
| [<span data-ttu-id="cf324-115">**GetContextNode**</span><span class="sxs-lookup"><span data-stu-id="cf324-115">**GetContextNode**</span></span>](icontextnodes-getcontextnode.md)       | <span data-ttu-id="cf324-116">Recupera el objeto [**IContextNode**](icontextnode.md) en el índice especificado de esta colección.</span><span class="sxs-lookup"><span data-stu-id="cf324-116">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span> <br/> |
| [<span data-ttu-id="cf324-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="cf324-117">**GetCount**</span></span>](icontextnodes-getcount.md)                   | <span data-ttu-id="cf324-118">Recupera el número de objetos [**IContextNode**](icontextnode.md) contenidos en esta colección.</span><span class="sxs-lookup"><span data-stu-id="cf324-118">Retrieves the number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span> <br/>       |
| [<span data-ttu-id="cf324-119">**RemoveContextNode**</span><span class="sxs-lookup"><span data-stu-id="cf324-119">**RemoveContextNode**</span></span>](icontextnodes-removecontextnode.md) | <span data-ttu-id="cf324-120">Quita un objeto [**IContextNode**](icontextnode.md) de esta colección.</span><span class="sxs-lookup"><span data-stu-id="cf324-120">Removes an [**IContextNode**](icontextnode.md) object from this collection.</span></span> <br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="cf324-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf324-121">Requirements</span></span>



| <span data-ttu-id="cf324-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf324-122">Requirement</span></span> | <span data-ttu-id="cf324-123">Value</span><span class="sxs-lookup"><span data-stu-id="cf324-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf324-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf324-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cf324-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cf324-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cf324-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf324-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cf324-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cf324-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cf324-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf324-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf324-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cf324-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cf324-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cf324-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf324-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf324-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cf324-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf324-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf324-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="cf324-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="cf324-134">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="cf324-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

