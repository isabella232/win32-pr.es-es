---
description: Recupera el IContextLink en el índice especificado.
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: 'IContextLinks:: GetContextLink (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ecc0ed9ba457a7a91cb2e1b615ac7419ce5a94c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154442"
---
# <a name="icontextlinksgetcontextlink-method"></a><span data-ttu-id="9ecba-103">IContextLinks:: GetContextLink (método)</span><span class="sxs-lookup"><span data-stu-id="9ecba-103">IContextLinks::GetContextLink method</span></span>

<span data-ttu-id="9ecba-104">Recupera el [**IContextLink**](icontextlink.md) en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="9ecba-104">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ecba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ecba-105">Syntax</span></span>


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a><span data-ttu-id="9ecba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ecba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ecba-107">*ulIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ecba-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ecba-108">Índice de base cero del objeto [**IContextLink**](icontextlink.md) que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="9ecba-108">The zero-based index of the [**IContextLink**](icontextlink.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="9ecba-109">*ppContextLink* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9ecba-109">*ppContextLink* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ecba-110">Puntero al objeto [**IContextLink**](icontextlink.md) en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="9ecba-110">A pointer to the [**IContextLink**](icontextlink.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ecba-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ecba-111">Return value</span></span>

<span data-ttu-id="9ecba-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9ecba-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ecba-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ecba-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9ecba-114">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextLink* cuando ya no necesite usar el vínculo de contexto.</span><span class="sxs-lookup"><span data-stu-id="9ecba-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLink* when you no longer need to use the context link.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ecba-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ecba-115">Requirements</span></span>



| <span data-ttu-id="9ecba-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ecba-116">Requirement</span></span> | <span data-ttu-id="9ecba-117">Value</span><span class="sxs-lookup"><span data-stu-id="9ecba-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ecba-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ecba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ecba-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9ecba-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9ecba-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ecba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ecba-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9ecba-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9ecba-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ecba-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ecba-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9ecba-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9ecba-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ecba-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ecba-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ecba-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9ecba-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ecba-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ecba-127">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="9ecba-127">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="9ecba-128">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="9ecba-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9ecba-129">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="9ecba-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

