---
title: min (macro) (Minwindef. h)
description: La macro min compara dos valores y devuelve el menor. El tipo de datos puede ser cualquier tipo de datos numérico, con signo o sin signo. El tipo de datos de los argumentos y el valor devuelto es el mismo.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- min macros multimedia de Windows
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50680d5902ae2dc895f53f023c4b229b03c7e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804094"
---
# <a name="min-macro"></a><span data-ttu-id="fd048-106">min (macro)</span><span class="sxs-lookup"><span data-stu-id="fd048-106">min macro</span></span>

<span data-ttu-id="fd048-107">La macro **min** compara dos valores y devuelve el menor.</span><span class="sxs-lookup"><span data-stu-id="fd048-107">The **min** macro compares two values and returns the smaller one.</span></span> <span data-ttu-id="fd048-108">El tipo de datos puede ser cualquier tipo de datos numérico, con signo o sin signo.</span><span class="sxs-lookup"><span data-stu-id="fd048-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="fd048-109">El tipo de datos de los argumentos y el valor devuelto es el mismo.</span><span class="sxs-lookup"><span data-stu-id="fd048-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd048-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd048-110">Syntax</span></span>


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="fd048-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd048-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd048-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="fd048-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="fd048-113">Especifica el primero de dos valores.</span><span class="sxs-lookup"><span data-stu-id="fd048-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="fd048-114">*value2*</span><span class="sxs-lookup"><span data-stu-id="fd048-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="fd048-115">Especifica el segundo de dos valores.</span><span class="sxs-lookup"><span data-stu-id="fd048-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd048-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd048-116">Return value</span></span>

<span data-ttu-id="fd048-117">El valor devuelto es el menor de los dos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="fd048-117">The return value is the smaller of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd048-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd048-118">Remarks</span></span>

<span data-ttu-id="fd048-119">La macro **min** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="fd048-119">The **min** macro is defined as follows:</span></span>


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="fd048-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd048-120">Requirements</span></span>



| <span data-ttu-id="fd048-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd048-121">Requirement</span></span> | <span data-ttu-id="fd048-122">Value</span><span class="sxs-lookup"><span data-stu-id="fd048-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd048-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd048-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fd048-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fd048-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fd048-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd048-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fd048-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd048-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fd048-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd048-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd048-128"><dt>Minwindef. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd048-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 





