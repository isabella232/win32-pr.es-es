---
description: Quita un IContextNode secundario.
ms.assetid: ed1d7b35-f6ba-4eff-888d-5cc492f02832
title: IContextNode::D método eleteSubNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ffcec19e13a3ad885b3b497f80322caf9365c91a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542067"
---
# <a name="icontextnodedeletesubnode-method"></a><span data-ttu-id="02389-103">IContextNode::D método eleteSubNode</span><span class="sxs-lookup"><span data-stu-id="02389-103">IContextNode::DeleteSubNode method</span></span>

<span data-ttu-id="02389-104">Quita un [**IContextNode**](icontextnode.md)secundario.</span><span class="sxs-lookup"><span data-stu-id="02389-104">Removes a child [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="02389-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02389-105">Syntax</span></span>


```C++
HRESULT DeleteSubNode(
  [in] IContextNode *pContextNodeToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="02389-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02389-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02389-107">*pContextNodeToDelete* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02389-107">*pContextNodeToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02389-108">[**IContextNode**](icontextnode.md) que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="02389-108">The [**IContextNode**](icontextnode.md) to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02389-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02389-109">Return value</span></span>

<span data-ttu-id="02389-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="02389-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="02389-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02389-111">Remarks</span></span>

<span data-ttu-id="02389-112">\_Se devuelve E INVALIDARG si el parámetro *pContextNodeToDelete* no es un elemento secundario de este objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="02389-112">E\_INVALIDARG is returned if the *pContextNodeToDelete* parameter is not a child of this [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="02389-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02389-113">Requirements</span></span>



| <span data-ttu-id="02389-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="02389-114">Requirement</span></span> | <span data-ttu-id="02389-115">Value</span><span class="sxs-lookup"><span data-stu-id="02389-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02389-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02389-116">Minimum supported client</span></span><br/> | <span data-ttu-id="02389-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="02389-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="02389-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02389-118">Minimum supported server</span></span><br/> | <span data-ttu-id="02389-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="02389-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="02389-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02389-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="02389-121"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="02389-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="02389-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="02389-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02389-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02389-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="02389-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="02389-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02389-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="02389-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="02389-126">**IContextNode::CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="02389-126">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="02389-127">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="02389-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




