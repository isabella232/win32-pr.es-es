---
description: Comprueba si un puntero está alineado con un límite especificado. En caso contrario, esta macro invoca la macro Assert. Se omite en las compilaciones comerciales.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: Macro DbgAssertAligned (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681058"
---
# <a name="dbgassertaligned-macro"></a><span data-ttu-id="024c6-105">DbgAssertAligned (macro)</span><span class="sxs-lookup"><span data-stu-id="024c6-105">DbgAssertAligned macro</span></span>

<span data-ttu-id="024c6-106">Comprueba si un puntero está alineado con un límite especificado.</span><span class="sxs-lookup"><span data-stu-id="024c6-106">Tests whether a pointer is aligned to a specified boundary.</span></span> <span data-ttu-id="024c6-107">En caso contrario, esta macro invoca la macro [**Assert**](assert.md) .</span><span class="sxs-lookup"><span data-stu-id="024c6-107">If not, this macro invokes the [**ASSERT**](assert.md) macro.</span></span> <span data-ttu-id="024c6-108">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="024c6-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="024c6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="024c6-109">Syntax</span></span>


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a><span data-ttu-id="024c6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="024c6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="024c6-111">*ptr*</span><span class="sxs-lookup"><span data-stu-id="024c6-111">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="024c6-112">Variable de puntero.</span><span class="sxs-lookup"><span data-stu-id="024c6-112">Pointer variable.</span></span>

</dd> <dt>

<span data-ttu-id="024c6-113">*ecuación*</span><span class="sxs-lookup"><span data-stu-id="024c6-113">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="024c6-114">Alineación requerida.</span><span class="sxs-lookup"><span data-stu-id="024c6-114">Required alignment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="024c6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="024c6-115">Return value</span></span>

<span data-ttu-id="024c6-116">Esta macro no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="024c6-116">This macro does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="024c6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="024c6-117">Requirements</span></span>



| <span data-ttu-id="024c6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="024c6-118">Requirement</span></span> | <span data-ttu-id="024c6-119">Value</span><span class="sxs-lookup"><span data-stu-id="024c6-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="024c6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="024c6-120">Header</span></span><br/> | <dl> <span data-ttu-id="024c6-121"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="024c6-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="024c6-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="024c6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024c6-123">Macros Assert y Breakpoint</span><span class="sxs-lookup"><span data-stu-id="024c6-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




