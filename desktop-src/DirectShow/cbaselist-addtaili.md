---
description: El método AddTailI agrega un elemento al final de la lista.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Método CBaseList. AddTailI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c702256d75a2de6f914838f5c3412a4308a7241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660996"
---
# <a name="cbaselistaddtaili-method"></a><span data-ttu-id="3d313-103">CBaseList. AddTailI, método</span><span class="sxs-lookup"><span data-stu-id="3d313-103">CBaseList.AddTailI method</span></span>

<span data-ttu-id="3d313-104">El `AddTailI` método agrega un elemento al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="3d313-104">The `AddTailI` method adds an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d313-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d313-105">Syntax</span></span>


```C++
POSITION AddTailI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="3d313-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d313-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d313-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="3d313-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="3d313-108">Puntero al elemento.</span><span class="sxs-lookup"><span data-stu-id="3d313-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d313-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d313-109">Return value</span></span>

<span data-ttu-id="3d313-110">Devuelve un valor de posición para la nueva posición de la cola.</span><span class="sxs-lookup"><span data-stu-id="3d313-110">Returns a POSITION value for the new tail position.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d313-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d313-111">Remarks</span></span>

<span data-ttu-id="3d313-112">Si se produce un error en el método, devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="3d313-112">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d313-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d313-113">Requirements</span></span>



| <span data-ttu-id="3d313-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d313-114">Requirement</span></span> | <span data-ttu-id="3d313-115">Value</span><span class="sxs-lookup"><span data-stu-id="3d313-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d313-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d313-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3d313-117"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d313-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3d313-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d313-118">Library</span></span><br/> | <dl> <span data-ttu-id="3d313-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3d313-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d313-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d313-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d313-121">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="3d313-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




