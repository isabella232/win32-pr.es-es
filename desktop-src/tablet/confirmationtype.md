---
description: Especifica el tipo de confirmación que se puede producir en un objeto IContextNode.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: Enumeración ConfirmationType (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 2c43971c6ccf44513c11e46d4bc5db86d973d7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714960"
---
# <a name="confirmationtype-enumeration"></a><span data-ttu-id="ad385-103">Enumeración ConfirmationType</span><span class="sxs-lookup"><span data-stu-id="ad385-103">ConfirmationType enumeration</span></span>

<span data-ttu-id="ad385-104">Especifica el tipo de confirmación que se puede producir en un objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ad385-104">Specifies the type of confirmation that can occur on an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad385-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad385-105">Syntax</span></span>


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a><span data-ttu-id="ad385-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ad385-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ad385-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="ad385-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType\_None**</span></span>
</dt> <dd>

<span data-ttu-id="ad385-108">No se aplica ninguna confirmación.</span><span class="sxs-lookup"><span data-stu-id="ad385-108">No confirmation is applied.</span></span> <span data-ttu-id="ad385-109">[**IInkAnalyzer**](iinkanalyzer.md) es libre de cambiar un nodo de contexto o cualquiera de sus descendientes según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ad385-109">The [**IInkAnalyzer**](iinkanalyzer.md) is free to change a context node or any of its descendants as needed.</span></span>

</dd> <dt>

<span data-ttu-id="ad385-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType \_ NodeTypeAndProperties**</span><span class="sxs-lookup"><span data-stu-id="ad385-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType\_NodeTypeAndProperties**</span></span>
</dt> <dd>

<span data-ttu-id="ad385-111">[**IInkAnalyzer**](iinkanalyzer.md) no puede cambiar el tipo ni ninguna propiedad del nodo de contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="ad385-111">The [**IInkAnalyzer**](iinkanalyzer.md) cannot change the type or any properties of the specified context node.</span></span>

</dd> <dt>

<span data-ttu-id="ad385-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**Límite de ConfirmationType \_**</span><span class="sxs-lookup"><span data-stu-id="ad385-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType\_TopBoundary**</span></span>
</dt> <dd>

<span data-ttu-id="ad385-113">El [**IInkAnalyzer**](iinkanalyzer.md) no realizará operaciones, incluida la adición de tinta o combinación con otros [**ContextNodes**](icontextnodes.md), lo que hace que el límite se mueva más allá del límite superior actual.</span><span class="sxs-lookup"><span data-stu-id="ad385-113">The [**IInkAnalyzer**](iinkanalyzer.md) will not perform operations, including adding ink or merging with other [**ContextNodes**](icontextnodes.md), that cause the TopBoundary to move beyond the current top boundary.</span></span> <span data-ttu-id="ad385-114">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ad385-114">For example:</span></span>

-   <span data-ttu-id="ad385-115">Una aplicación analiza un conjunto de entradas de lápiz y se identifica un ParagraphNode.</span><span class="sxs-lookup"><span data-stu-id="ad385-115">An application analyzes a set of Ink, and a ParagraphNode is identified.</span></span>
-   <span data-ttu-id="ad385-116">La aplicación confirma el límite de este párrafo.</span><span class="sxs-lookup"><span data-stu-id="ad385-116">The application confirms the TopBoundary of this paragraph.</span></span>
-   <span data-ttu-id="ad385-117">El usuario de la aplicación escribe una nueva entrada de lápiz sobre el párrafo actual.</span><span class="sxs-lookup"><span data-stu-id="ad385-117">The user of the application writes new ink above the current paragraph.</span></span> <span data-ttu-id="ad385-118">Cuando se llama de nuevo a Analyze, la nueva entrada de lápiz no se incorporará en el nodo de párrafo confirmado.</span><span class="sxs-lookup"><span data-stu-id="ad385-118">When analyze is called again, the new ink will not be incorporated into the Confirmed paragraph node.</span></span>
-   <span data-ttu-id="ad385-119">Dado que solo se confirma el límite superior, el ContextNode puede seguir creciendo en otras direcciones.</span><span class="sxs-lookup"><span data-stu-id="ad385-119">Since only the top boundary is confirmed, the ContextNode can continue to grow in other directions.</span></span> <span data-ttu-id="ad385-120">La eliminación de trazos puede hacer que el límite superior se desplace hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="ad385-120">Deleting strokes can cause the top boundary to move down.</span></span> <span data-ttu-id="ad385-121">La traducción de ContextNode puede hacer que la ubicación cambie, pero no permite la combinación de tinta adicional en la nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="ad385-121">Translating the ContextNode can cause the location to change, but will not allow additional ink to be merged in the new location.</span></span>

<span data-ttu-id="ad385-122">Este ConfirmationType solo es aplicable a los nodos de párrafo.</span><span class="sxs-lookup"><span data-stu-id="ad385-122">This ConfirmationType is only applicable to paragraph nodes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad385-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad385-123">Remarks</span></span>

<span data-ttu-id="ad385-124">Puede usar el valor **NodeTypeAndProperties** solo para los nodos de dibujo de tinta y de lápiz (vea [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="ad385-124">You can use the **NodeTypeAndProperties** value only for ink word and ink drawing nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="ad385-125">De lo contrario, se devuelve un **E \_ INVALIDARG** de [**IContextNode:: CONFIRM**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="ad385-125">Otherwise, an **E\_INVALIDARG** is returned from [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad385-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad385-126">Requirements</span></span>



| <span data-ttu-id="ad385-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad385-127">Requirement</span></span> | <span data-ttu-id="ad385-128">Value</span><span class="sxs-lookup"><span data-stu-id="ad385-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad385-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad385-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ad385-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ad385-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ad385-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad385-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ad385-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ad385-132">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ad385-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad385-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad385-134"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ad385-134"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad385-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad385-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad385-136">**IContextNode:: CONFIRM**</span><span class="sxs-lookup"><span data-stu-id="ad385-136">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="ad385-137">**IContextNode::IsConfirmed**</span><span class="sxs-lookup"><span data-stu-id="ad385-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




