---
description: El método AddAfter inserta una lista después de la posición especificada.
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: Método CBaseList. AddAfter (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdab54a124986b462e0ef592bba888e27c09b53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660680"
---
# <a name="cbaselistaddafter-method"></a><span data-ttu-id="6283d-103">CBaseList. AddAfter, método</span><span class="sxs-lookup"><span data-stu-id="6283d-103">CBaseList.AddAfter method</span></span>

<span data-ttu-id="6283d-104">El `AddAfter` método inserta una lista después de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="6283d-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="6283d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6283d-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="6283d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6283d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6283d-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="6283d-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="6283d-108">Posición después de la cual se va a insertar la lista.</span><span class="sxs-lookup"><span data-stu-id="6283d-108">Position after which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="6283d-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="6283d-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="6283d-110">Puntero a la lista que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="6283d-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6283d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6283d-111">Return value</span></span>

<span data-ttu-id="6283d-112">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6283d-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6283d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6283d-113">Remarks</span></span>

<span data-ttu-id="6283d-114">Los indicadores de posición existentes, incluido el especificado en el parámetro *pos* , siguen siendo válidos.</span><span class="sxs-lookup"><span data-stu-id="6283d-114">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="6283d-115">Si se produce un error en el método, es posible que se hayan agregado algunos elementos.</span><span class="sxs-lookup"><span data-stu-id="6283d-115">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="6283d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6283d-116">Requirements</span></span>



| <span data-ttu-id="6283d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6283d-117">Requirement</span></span> | <span data-ttu-id="6283d-118">Value</span><span class="sxs-lookup"><span data-stu-id="6283d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6283d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6283d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6283d-120"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6283d-120"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6283d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6283d-121">Library</span></span><br/> | <dl> <span data-ttu-id="6283d-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6283d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6283d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6283d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6283d-124">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="6283d-124">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




