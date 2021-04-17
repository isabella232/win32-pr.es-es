---
description: El método AlignDown trunca un valor en un límite de alineación especificado.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Método CPullPin. AlignDown (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1383517f4931fa153fd141878475cc8775a61045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680278"
---
# <a name="cpullpinaligndown-method"></a><span data-ttu-id="68e8a-103">CPullPin. AlignDown, método</span><span class="sxs-lookup"><span data-stu-id="68e8a-103">CPullPin.AlignDown method</span></span>

<span data-ttu-id="68e8a-104">El `AlignDown` método trunca un valor en un límite de alineación especificado.</span><span class="sxs-lookup"><span data-stu-id="68e8a-104">The `AlignDown` method truncates a value to a specified alignment boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e8a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68e8a-105">Syntax</span></span>


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="68e8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68e8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68e8a-107">*ll*</span><span class="sxs-lookup"><span data-stu-id="68e8a-107">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="68e8a-108">Especifica el número que se va a alinear.</span><span class="sxs-lookup"><span data-stu-id="68e8a-108">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="68e8a-109">*lAlign*</span><span class="sxs-lookup"><span data-stu-id="68e8a-109">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="68e8a-110">Especifica el límite de alineación.</span><span class="sxs-lookup"><span data-stu-id="68e8a-110">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68e8a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68e8a-111">Return value</span></span>

<span data-ttu-id="68e8a-112">Devuelve el resultado alineado.</span><span class="sxs-lookup"><span data-stu-id="68e8a-112">Returns the aligned result.</span></span>

## <a name="requirements"></a><span data-ttu-id="68e8a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68e8a-113">Requirements</span></span>



| <span data-ttu-id="68e8a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="68e8a-114">Requirement</span></span> | <span data-ttu-id="68e8a-115">Value</span><span class="sxs-lookup"><span data-stu-id="68e8a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68e8a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68e8a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="68e8a-117"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="68e8a-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="68e8a-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68e8a-118">Library</span></span><br/> | <dl> <span data-ttu-id="68e8a-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="68e8a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68e8a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="68e8a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e8a-121">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="68e8a-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




