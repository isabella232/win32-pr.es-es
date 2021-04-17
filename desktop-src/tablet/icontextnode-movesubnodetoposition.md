---
description: Reordena un objeto IContextNode secundario especificado al índice especificado.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'IContextNode:: MoveSubNodeToPosition (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696529"
---
# <a name="icontextnodemovesubnodetoposition-method"></a><span data-ttu-id="6b894-103">IContextNode:: MoveSubNodeToPosition (método)</span><span class="sxs-lookup"><span data-stu-id="6b894-103">IContextNode::MoveSubNodeToPosition method</span></span>

<span data-ttu-id="6b894-104">Reordena un objeto [**IContextNode**](icontextnode.md) secundario especificado al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="6b894-104">Reorders a specified child [**IContextNode**](icontextnode.md) object to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b894-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b894-105">Syntax</span></span>


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="6b894-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b894-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b894-107">*pSubnodeToMove* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6b894-107">*pSubnodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b894-108">Objeto [**IContextNode**](icontextnode.md) que se va a desplace.</span><span class="sxs-lookup"><span data-stu-id="6b894-108">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="6b894-109">*ulNewIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6b894-109">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b894-110">Índice de la nueva posición del subnodo.</span><span class="sxs-lookup"><span data-stu-id="6b894-110">The index for the new position of the subnode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b894-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b894-111">Return value</span></span>

<span data-ttu-id="6b894-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6b894-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b894-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b894-113">Remarks</span></span>

<span data-ttu-id="6b894-114">Devuelve **E \_ INVALIDARG** si *pSubnodeToMove* no es un nodo secundario de este [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="6b894-114">Returns **E\_INVALIDARG** if *pSubnodeToMove* is not a child node of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b894-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b894-115">Requirements</span></span>



| <span data-ttu-id="6b894-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b894-116">Requirement</span></span> | <span data-ttu-id="6b894-117">Value</span><span class="sxs-lookup"><span data-stu-id="6b894-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b894-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b894-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6b894-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6b894-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6b894-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b894-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6b894-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6b894-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6b894-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b894-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b894-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6b894-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6b894-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b894-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b894-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b894-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6b894-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b894-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b894-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="6b894-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6b894-128">**IContextNode::CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="6b894-128">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="6b894-129">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="6b894-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




