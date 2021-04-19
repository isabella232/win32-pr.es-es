---
description: Mueve los datos de trazo desde este IContextNode al IContextNode especificado.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'IContextNode:: ReparentStrokeByIdToNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3984153a0551de999563b8775ceb5acba1696e39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696528"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a><span data-ttu-id="6f26d-103">IContextNode:: ReparentStrokeByIdToNode (método)</span><span class="sxs-lookup"><span data-stu-id="6f26d-103">IContextNode::ReparentStrokeByIdToNode method</span></span>

<span data-ttu-id="6f26d-104">Mueve los datos de trazo desde este [**IContextNode**](icontextnode.md) al **IContextNode** especificado.</span><span class="sxs-lookup"><span data-stu-id="6f26d-104">Moves stroke data from this [**IContextNode**](icontextnode.md) to the specified **IContextNode**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f26d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f26d-105">Syntax</span></span>


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a><span data-ttu-id="6f26d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f26d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f26d-107">*lStrokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f26d-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f26d-108">Identificador del trazo que se va a desplace.</span><span class="sxs-lookup"><span data-stu-id="6f26d-108">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="6f26d-109">*pContextNodeDestination* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f26d-109">*pContextNodeDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f26d-110">Objeto [**IContextNode**](icontextnode.md) al que se van a trasladar los datos del trazo.</span><span class="sxs-lookup"><span data-stu-id="6f26d-110">The [**IContextNode**](icontextnode.md) object to which to move the stroke data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f26d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f26d-111">Return value</span></span>

<span data-ttu-id="6f26d-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6f26d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f26d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f26d-113">Remarks</span></span>

<span data-ttu-id="6f26d-114">El objeto [**IContextNode**](icontextnode.md) especificado debe ser uno de los siguientes tipos de las constantes de [tipos de nodo de contexto](context-node-types.md) : **InkWord**, **InkDrawing**, **InkBullet** o **UnclassifiedInk**.</span><span class="sxs-lookup"><span data-stu-id="6f26d-114">The specified [**IContextNode**](icontextnode.md) object must be one of the following types from the [Context Node Types](context-node-types.md) constants: **InkWord**, **InkDrawing**, **InkBullet**, or **UnclassifiedInk**.</span></span> <span data-ttu-id="6f26d-115">Al intentar desplace un trazo a cualquier otro tipo de objeto **IContextNode** , se obtiene un valor devuelto de **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="6f26d-115">Attempting to move a stroke to any other type of **IContextNode** object results in a return value of **E\_INVALIDARG**.</span></span>

<span data-ttu-id="6f26d-116">Se puede llamar a este método desde cualquier objeto [**IContextNode**](icontextnode.md) , incluidos los objetos **IContextNode** de hojas que no son de tinta.</span><span class="sxs-lookup"><span data-stu-id="6f26d-116">This method can be called from any [**IContextNode**](icontextnode.md) object, including non-ink leaf **IContextNode** objects.</span></span> <span data-ttu-id="6f26d-117">Uno de los descendientes de este objeto **IContextNode** debe hacer referencia al trazo especificado o se devuelve **E \_ INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="6f26d-117">The specified stroke must be referenced by one of the descendants of this **IContextNode** object or **E\_INVALIDARG** is returned.</span></span>

<span data-ttu-id="6f26d-118">Si se confirma este [**IContextNode**](icontextnode.md) o **IContextNode** en *pContextNodeDestination* , se devuelve **E \_ INVALIDARG** (vea [**IContextNode:: IsConfirmed**](icontextnode-isconfirmed.md)).</span><span class="sxs-lookup"><span data-stu-id="6f26d-118">If either this [**IContextNode**](icontextnode.md) or the **IContextNode** in *pContextNodeDestination* is confirmed, **E\_INVALIDARG** is returned (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)).</span></span>

<span data-ttu-id="6f26d-119">El analizador de tinta no elimina los nodos de contexto vacíos de su árbol de resultados en respuesta a este método.</span><span class="sxs-lookup"><span data-stu-id="6f26d-119">The ink analyzer does not delete empty context nodes from its results tree in response to this method.</span></span>

-   <span data-ttu-id="6f26d-120">Un nodo de hoja de tinta que no hace referencia a ningún dato de trazo es un nodo vacío.</span><span class="sxs-lookup"><span data-stu-id="6f26d-120">An ink leaf node that does not reference any stroke data is an empty node.</span></span>
-   <span data-ttu-id="6f26d-121">Un nodo contenedor que no hace referencia A los nodos secundarios es un nodo vacío.</span><span class="sxs-lookup"><span data-stu-id="6f26d-121">A container node that does not reference any child nodes is an empty node.</span></span>

<span data-ttu-id="6f26d-122">Un nodo vacío genera errores si se encuentra en el árbol durante una operación de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="6f26d-122">An empty node generates errors if it is in the tree during an ink analysis operation.</span></span> <span data-ttu-id="6f26d-123">Para quitar un nodo del árbol del analizador de tinta, llame al método [**IContextNode::D eletesubnode**](icontextnode-deletesubnode.md) del nodo primario (consulte [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md)).</span><span class="sxs-lookup"><span data-stu-id="6f26d-123">To remove a node from the ink analyzer's tree, call the parent node's [**IContextNode::DeleteSubNode**](icontextnode-deletesubnode.md) method (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f26d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f26d-124">Requirements</span></span>



| <span data-ttu-id="6f26d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f26d-125">Requirement</span></span> | <span data-ttu-id="6f26d-126">Value</span><span class="sxs-lookup"><span data-stu-id="6f26d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f26d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f26d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6f26d-128">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6f26d-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6f26d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f26d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6f26d-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6f26d-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6f26d-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f26d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f26d-132"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6f26d-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6f26d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f26d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f26d-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f26d-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6f26d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f26d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f26d-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="6f26d-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6f26d-137">**IContextNode::SetStrokes**</span><span class="sxs-lookup"><span data-stu-id="6f26d-137">**IContextNode::SetStrokes**</span></span>](icontextnode-setstrokes.md)
</dt> <dt>

[<span data-ttu-id="6f26d-138">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="6f26d-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




