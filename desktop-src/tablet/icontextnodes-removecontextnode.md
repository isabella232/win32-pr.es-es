---
description: Quita un objeto IContextNode de esta colección.
ms.assetid: ddda506d-4e39-486d-ac7d-211dc7869a73
title: 'IContextNodes:: RemoveContextNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.RemoveContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 371722cca3d8ccc132c151b37e9d1a469bdb0c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715223"
---
# <a name="icontextnodesremovecontextnode-method"></a><span data-ttu-id="64175-103">IContextNodes:: RemoveContextNode (método)</span><span class="sxs-lookup"><span data-stu-id="64175-103">IContextNodes::RemoveContextNode method</span></span>

<span data-ttu-id="64175-104">Quita un objeto [**IContextNode**](icontextnode.md) de esta colección.</span><span class="sxs-lookup"><span data-stu-id="64175-104">Removes an [**IContextNode**](icontextnode.md) object from this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="64175-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64175-105">Syntax</span></span>


```C++
HRESULT RemoveContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="64175-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64175-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64175-107">*pContextNode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64175-107">*pContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64175-108">Objeto [**IContextNode**](icontextnode.md) que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="64175-108">The [**IContextNode**](icontextnode.md) object to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64175-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64175-109">Return value</span></span>

<span data-ttu-id="64175-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="64175-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64175-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64175-111">Requirements</span></span>



| <span data-ttu-id="64175-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="64175-112">Requirement</span></span> | <span data-ttu-id="64175-113">Value</span><span class="sxs-lookup"><span data-stu-id="64175-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64175-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64175-114">Minimum supported client</span></span><br/> | <span data-ttu-id="64175-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="64175-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="64175-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64175-116">Minimum supported server</span></span><br/> | <span data-ttu-id="64175-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="64175-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="64175-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64175-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="64175-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="64175-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="64175-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="64175-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64175-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64175-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="64175-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="64175-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64175-123">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="64175-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="64175-124">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="64175-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




