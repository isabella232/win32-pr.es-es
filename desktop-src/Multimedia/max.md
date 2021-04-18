---
title: Max (macro) (Minwindef. h)
description: La macro Max compara dos valores y devuelve el más grande. El tipo de datos puede ser cualquier tipo de datos numérico, con signo o sin signo. El tipo de datos de los argumentos y el valor devuelto es el mismo.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- macros máximas de Windows multimedia
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b484f2505958aca04745c63ca63a0dd131a51ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534018"
---
# <a name="max-macro"></a><span data-ttu-id="a4084-106">max (macro)</span><span class="sxs-lookup"><span data-stu-id="a4084-106">max macro</span></span>

<span data-ttu-id="a4084-107">La macro **Max** compara dos valores y devuelve el más grande.</span><span class="sxs-lookup"><span data-stu-id="a4084-107">The **max** macro compares two values and returns the larger one.</span></span> <span data-ttu-id="a4084-108">El tipo de datos puede ser cualquier tipo de datos numérico, con signo o sin signo.</span><span class="sxs-lookup"><span data-stu-id="a4084-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="a4084-109">El tipo de datos de los argumentos y el valor devuelto es el mismo.</span><span class="sxs-lookup"><span data-stu-id="a4084-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4084-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4084-110">Syntax</span></span>


```C++
 max(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="a4084-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4084-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4084-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="a4084-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="a4084-113">Especifica el primero de dos valores.</span><span class="sxs-lookup"><span data-stu-id="a4084-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="a4084-114">*value2*</span><span class="sxs-lookup"><span data-stu-id="a4084-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="a4084-115">Especifica el segundo de dos valores.</span><span class="sxs-lookup"><span data-stu-id="a4084-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4084-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4084-116">Return value</span></span>

<span data-ttu-id="a4084-117">El valor devuelto es el mayor de los dos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="a4084-117">The return value is the greater of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4084-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4084-118">Remarks</span></span>

<span data-ttu-id="a4084-119">La macro **Max** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a4084-119">The **max** macro is defined as follows:</span></span>


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="a4084-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4084-120">Requirements</span></span>



| <span data-ttu-id="a4084-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4084-121">Requirement</span></span> | <span data-ttu-id="a4084-122">Value</span><span class="sxs-lookup"><span data-stu-id="a4084-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4084-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4084-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a4084-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a4084-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a4084-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4084-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a4084-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a4084-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a4084-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4084-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4084-128"><dt>Minwindef. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4084-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 





