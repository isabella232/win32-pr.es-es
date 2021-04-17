---
description: El método AddBefore inserta una lista antes de la posición especificada.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Método CBaseList. AddBefore (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3c25b2dd545b3e6698404bf00f82d1086bfb81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660679"
---
# <a name="cbaselistaddbefore-method"></a><span data-ttu-id="662a8-103">CBaseList. AddBefore, método</span><span class="sxs-lookup"><span data-stu-id="662a8-103">CBaseList.AddBefore method</span></span>

<span data-ttu-id="662a8-104">El `AddBefore` método inserta una lista antes de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="662a8-104">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="662a8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="662a8-105">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="662a8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="662a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="662a8-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="662a8-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="662a8-108">Posición antes de la que se va a insertar la lista.</span><span class="sxs-lookup"><span data-stu-id="662a8-108">Position before which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="662a8-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="662a8-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="662a8-110">Puntero a la lista que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="662a8-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="662a8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="662a8-111">Return value</span></span>

<span data-ttu-id="662a8-112">Devuelve **true si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="662a8-112">Returns **TRUE** if successful.</span></span> <span data-ttu-id="662a8-113">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="662a8-113">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="662a8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="662a8-114">Remarks</span></span>

<span data-ttu-id="662a8-115">Los indicadores de posición existentes, incluido el especificado en el parámetro *pos* , siguen siendo válidos.</span><span class="sxs-lookup"><span data-stu-id="662a8-115">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="662a8-116">Si se produce un error en el método, es posible que se hayan agregado algunos elementos.</span><span class="sxs-lookup"><span data-stu-id="662a8-116">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="662a8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="662a8-117">Requirements</span></span>



| <span data-ttu-id="662a8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="662a8-118">Requirement</span></span> | <span data-ttu-id="662a8-119">Value</span><span class="sxs-lookup"><span data-stu-id="662a8-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="662a8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="662a8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="662a8-121"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="662a8-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="662a8-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="662a8-122">Library</span></span><br/> | <dl> <span data-ttu-id="662a8-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="662a8-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="662a8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="662a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="662a8-125">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="662a8-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




