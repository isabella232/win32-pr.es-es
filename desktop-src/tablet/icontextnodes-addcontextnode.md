---
description: Agrega un objeto IContextNode a esta colección.
ms.assetid: 48feae05-1cc8-46c3-97cd-4493ee28b8e5
title: 'IContextNodes:: AddContextNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.AddContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 18a7438c09fb2a850637bbae549ada61c37fb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154430"
---
# <a name="icontextnodesaddcontextnode-method"></a><span data-ttu-id="7b603-103">IContextNodes:: AddContextNode (método)</span><span class="sxs-lookup"><span data-stu-id="7b603-103">IContextNodes::AddContextNode method</span></span>

<span data-ttu-id="7b603-104">Agrega un objeto [**IContextNode**](icontextnode.md) a esta colección.</span><span class="sxs-lookup"><span data-stu-id="7b603-104">Adds an [**IContextNode**](icontextnode.md) object to this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b603-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b603-105">Syntax</span></span>


```C++
HRESULT AddContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="7b603-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b603-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b603-107">*pContextNode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7b603-107">*pContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b603-108">Objeto [**IContextNode**](icontextnode.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="7b603-108">The [**IContextNode**](icontextnode.md) object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b603-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b603-109">Return value</span></span>

<span data-ttu-id="7b603-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7b603-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b603-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b603-111">Requirements</span></span>



| <span data-ttu-id="7b603-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b603-112">Requirement</span></span> | <span data-ttu-id="7b603-113">Value</span><span class="sxs-lookup"><span data-stu-id="7b603-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b603-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b603-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7b603-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7b603-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7b603-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b603-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7b603-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7b603-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7b603-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b603-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b603-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7b603-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7b603-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7b603-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b603-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b603-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7b603-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b603-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b603-123">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="7b603-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="7b603-124">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="7b603-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




