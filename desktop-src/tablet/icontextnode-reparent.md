---
description: Mueve este objeto IContextNode de la colección de subnodos del nodo de contexto primario a la colección de subnodos del nodo de contexto especificado.
ms.assetid: e19ecbe3-f7aa-499c-86a1-236dc9056fd9
title: 'Método IContextNode:: reparent (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Reparent
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 805b96b2a392a4f7b70aa4ce5913b48ffaf33551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082156"
---
# <a name="icontextnodereparent-method"></a><span data-ttu-id="a2c61-103">IContextNode:: reparent (método)</span><span class="sxs-lookup"><span data-stu-id="a2c61-103">IContextNode::Reparent method</span></span>

<span data-ttu-id="a2c61-104">Mueve este objeto [**IContextNode**](icontextnode.md) de la colección de subnodos del nodo de contexto primario a la colección de subnodos del nodo de contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="a2c61-104">Moves this [**IContextNode**](icontextnode.md) object from its parent context node's collection of subnodes to the specified context node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c61-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2c61-105">Syntax</span></span>


```C++
HRESULT Reparent(
  [in] IContextNode *pNewParent
);
```



## <a name="parameters"></a><span data-ttu-id="a2c61-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2c61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2c61-107">*pNewParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a2c61-107">*pNewParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2c61-108">Nuevo nodo primario de este objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c61-108">The new parent node for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2c61-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2c61-109">Return value</span></span>

<span data-ttu-id="a2c61-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a2c61-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2c61-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2c61-111">Requirements</span></span>



| <span data-ttu-id="a2c61-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2c61-112">Requirement</span></span> | <span data-ttu-id="a2c61-113">Value</span><span class="sxs-lookup"><span data-stu-id="a2c61-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c61-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2c61-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a2c61-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a2c61-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a2c61-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2c61-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a2c61-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a2c61-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a2c61-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2c61-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2c61-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a2c61-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a2c61-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a2c61-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2c61-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2c61-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a2c61-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2c61-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c61-123">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="a2c61-123">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="a2c61-124">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="a2c61-124">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="a2c61-125">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="a2c61-125">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="a2c61-126">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="a2c61-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




