---
description: Recupera un valor que indica si se ha establecido en este IContextNode el ConfirmationType pasado a este método.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'IContextNode:: IsConfirmed (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 300e0126b4a1ff55d372ff31deebde0eab686645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542051"
---
# <a name="icontextnodeisconfirmed-method"></a><span data-ttu-id="bd3cf-103">IContextNode:: IsConfirmed (método)</span><span class="sxs-lookup"><span data-stu-id="bd3cf-103">IContextNode::IsConfirmed method</span></span>

<span data-ttu-id="bd3cf-104">Recupera un valor que indica si se ha establecido en este IContextNode el ConfirmationType pasado a este método.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-104">Retrieves a value that indicates whether the ConfirmationType passed in to this method has been set on this IContextNode.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd3cf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd3cf-105">Syntax</span></span>


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a><span data-ttu-id="bd3cf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd3cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd3cf-107">*confirmedType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd3cf-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3cf-108">El tipo de confirmación que se está probando.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-108">The confirmation type being tested for.</span></span>

</dd> <dt>

<span data-ttu-id="bd3cf-109">*pfTypeConfirmed* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bd3cf-109">*pfTypeConfirmed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3cf-110">**Variante \_ TRUE** si el tipo pasado en confirmedType se ha establecido en este objeto [**IContextNode**](icontextnode.md) ; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-110">**VARIANT\_TRUE** if the type passed in confirmedType has been set on this [**IContextNode**](icontextnode.md) object; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd3cf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd3cf-111">Return value</span></span>

<span data-ttu-id="bd3cf-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bd3cf-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd3cf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd3cf-113">Remarks</span></span>

<span data-ttu-id="bd3cf-114">Este valor se establece mediante el método [**IContextNode:: CONFIRM**](icontextnode-confirm.md) .</span><span class="sxs-lookup"><span data-stu-id="bd3cf-114">This value is set by the [**IContextNode::Confirm**](icontextnode-confirm.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd3cf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd3cf-115">Requirements</span></span>



| <span data-ttu-id="bd3cf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd3cf-116">Requirement</span></span> | <span data-ttu-id="bd3cf-117">Value</span><span class="sxs-lookup"><span data-stu-id="bd3cf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd3cf-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd3cf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bd3cf-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bd3cf-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bd3cf-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd3cf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bd3cf-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bd3cf-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bd3cf-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd3cf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd3cf-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bd3cf-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bd3cf-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd3cf-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd3cf-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd3cf-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bd3cf-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd3cf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd3cf-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="bd3cf-128">**IContextNode:: CONFIRM**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-128">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="bd3cf-129">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="bd3cf-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




