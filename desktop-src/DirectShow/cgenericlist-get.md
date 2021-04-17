---
description: El método get recupera el elemento en la posición especificada.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: Método CGenericList. get (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02af7d57d2219e6eb0506a8ab11521b4cf3570eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671144"
---
# <a name="cgenericlistget-method"></a><span data-ttu-id="63ec2-103">CGenericList. get (método)</span><span class="sxs-lookup"><span data-stu-id="63ec2-103">CGenericList.Get method</span></span>

<span data-ttu-id="63ec2-104">El `Get` método recupera el elemento en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="63ec2-104">The `Get` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="63ec2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63ec2-105">Syntax</span></span>


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="63ec2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63ec2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63ec2-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="63ec2-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="63ec2-108">Indicador de posición del elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="63ec2-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63ec2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63ec2-109">Return value</span></span>

<span data-ttu-id="63ec2-110">Devuelve un puntero a un objeto de tipo **Object** (el tipo de plantilla).</span><span class="sxs-lookup"><span data-stu-id="63ec2-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="63ec2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63ec2-111">Remarks</span></span>

<span data-ttu-id="63ec2-112">Si *pos* es **null**, el método devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="63ec2-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="63ec2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63ec2-113">Requirements</span></span>



| <span data-ttu-id="63ec2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="63ec2-114">Requirement</span></span> | <span data-ttu-id="63ec2-115">Value</span><span class="sxs-lookup"><span data-stu-id="63ec2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ec2-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63ec2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="63ec2-117"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63ec2-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="63ec2-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63ec2-118">Library</span></span><br/> | <dl> <span data-ttu-id="63ec2-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="63ec2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63ec2-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="63ec2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ec2-121">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="63ec2-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




