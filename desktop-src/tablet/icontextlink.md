---
description: Representa una relación entre dos objetos IContextNode.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Interfaz IContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df1e0d8717ba29532486277aced19f17adb1d79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715233"
---
# <a name="icontextlink-interface"></a><span data-ttu-id="655f7-103">Interfaz IContextLink</span><span class="sxs-lookup"><span data-stu-id="655f7-103">IContextLink interface</span></span>

<span data-ttu-id="655f7-104">Representa una relación entre dos objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="655f7-104">Represents a relationship between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="655f7-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="655f7-105">Members</span></span>

<span data-ttu-id="655f7-106">La interfaz **IContextLink** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="655f7-106">The **IContextLink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="655f7-107">**IContextLink** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="655f7-107">**IContextLink** also has these types of members:</span></span>

-   [<span data-ttu-id="655f7-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="655f7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="655f7-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="655f7-109">Methods</span></span>

<span data-ttu-id="655f7-110">La interfaz **IContextLink** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="655f7-110">The **IContextLink** interface has these methods.</span></span>



| <span data-ttu-id="655f7-111">Método</span><span class="sxs-lookup"><span data-stu-id="655f7-111">Method</span></span>                                                                  | <span data-ttu-id="655f7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="655f7-112">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="655f7-113">**GetContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="655f7-113">**GetContextLinkDirection**</span></span>](icontextlink-getcontextlinkdirection.md) | <span data-ttu-id="655f7-114">Recupera el tipo de relación que representa este **IContextLink** .</span><span class="sxs-lookup"><span data-stu-id="655f7-114">Retrieves the type of relationship this **IContextLink** represents.</span></span><br/>                                         |
| [<span data-ttu-id="655f7-115">**GetDestinationNode**</span><span class="sxs-lookup"><span data-stu-id="655f7-115">**GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)           | <span data-ttu-id="655f7-116">Recupera el objeto [**IContextNode**](icontextnode.md) que es el destino de este **IContextLink**.</span><span class="sxs-lookup"><span data-stu-id="655f7-116">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this **IContextLink**.</span></span><br/> |
| [<span data-ttu-id="655f7-117">**GetSourceNode**</span><span class="sxs-lookup"><span data-stu-id="655f7-117">**GetSourceNode**</span></span>](icontextlink-getsourcenode.md)                     | <span data-ttu-id="655f7-118">Recupera el objeto [**IContextNode**](icontextnode.md) que es el origen de este **IContextLink**.</span><span class="sxs-lookup"><span data-stu-id="655f7-118">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this **IContextLink**.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="655f7-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="655f7-119">Remarks</span></span>

<span data-ttu-id="655f7-120">A continuación se presenta un ejemplo de una relación que se representa mediante un objeto **IContextLink** :</span><span class="sxs-lookup"><span data-stu-id="655f7-120">The following is an example of a relationship represented by an **IContextLink** object:</span></span>

-   <span data-ttu-id="655f7-121">Cuando se usa un nodo AnalysisHint en el análisis de tinta, la operación de análisis de tinta crea un objeto **IContextLink** de tipo AnalysisHint entre el nodo de sugerencia de análisis y el nodo que contiene la escritura dentro del área de la sugerencia.</span><span class="sxs-lookup"><span data-stu-id="655f7-121">When an AnalysisHint node is used in ink analysis, the ink analysis operation creates an **IContextLink** object of type AnalysisHint between the analysis hint node and the node that contains writing within the area of the hint.</span></span> <span data-ttu-id="655f7-122">El nodo de origen es el nodo de sugerencia de análisis y el nodo de destino es el nodo que contiene la escritura.</span><span class="sxs-lookup"><span data-stu-id="655f7-122">The source node is the analysis hint node and the destination node is the node that contains writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="655f7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="655f7-123">Requirements</span></span>



| <span data-ttu-id="655f7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="655f7-124">Requirement</span></span> | <span data-ttu-id="655f7-125">Value</span><span class="sxs-lookup"><span data-stu-id="655f7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="655f7-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="655f7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="655f7-127">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="655f7-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="655f7-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="655f7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="655f7-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="655f7-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="655f7-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="655f7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="655f7-131"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="655f7-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="655f7-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="655f7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="655f7-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="655f7-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="655f7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="655f7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="655f7-135">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="655f7-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="655f7-136">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="655f7-136">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="655f7-137">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="655f7-137">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="655f7-138">Tipos de nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="655f7-138">Context Node Types</span></span>](context-node-types.md)
</dt> </dl>

 

