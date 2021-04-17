---
description: El método MoveToTail divide la lista y anexa la parte del encabezado a la cola de otra lista.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: Método CBaseList. MoveToTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c28e1051c08884e70e56b25b0fb2707ccd55ed1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660666"
---
# <a name="cbaselistmovetotail-method"></a><span data-ttu-id="99a0f-103">CBaseList. MoveToTail, método</span><span class="sxs-lookup"><span data-stu-id="99a0f-103">CBaseList.MoveToTail method</span></span>

<span data-ttu-id="99a0f-104">El `MoveToTail` método divide la lista y anexa la parte del encabezado a la cola de otra lista.</span><span class="sxs-lookup"><span data-stu-id="99a0f-104">The `MoveToTail` method splits the list and appends the head portion to the tail of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="99a0f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99a0f-105">Syntax</span></span>


```C++
BOOL MoveToTail(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="99a0f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99a0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99a0f-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="99a0f-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="99a0f-108">Indicador de posición que marca la división en la lista.</span><span class="sxs-lookup"><span data-stu-id="99a0f-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="99a0f-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="99a0f-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="99a0f-110">Puntero a otra lista.</span><span class="sxs-lookup"><span data-stu-id="99a0f-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99a0f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99a0f-111">Return value</span></span>

<span data-ttu-id="99a0f-112">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="99a0f-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="99a0f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99a0f-113">Remarks</span></span>

<span data-ttu-id="99a0f-114">Este método divide la lista después de la posición especificada por el parámetro *pos* .</span><span class="sxs-lookup"><span data-stu-id="99a0f-114">This method splits the list after the position specified by the *pos* parameter.</span></span> <span data-ttu-id="99a0f-115">La parte del final permanece en la lista.</span><span class="sxs-lookup"><span data-stu-id="99a0f-115">The tail portion remains in the list.</span></span> <span data-ttu-id="99a0f-116">La parte del encabezado se anexa a la cola de la otra lista.</span><span class="sxs-lookup"><span data-stu-id="99a0f-116">The head portion is appended to the tail of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="99a0f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99a0f-117">Requirements</span></span>



| <span data-ttu-id="99a0f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="99a0f-118">Requirement</span></span> | <span data-ttu-id="99a0f-119">Value</span><span class="sxs-lookup"><span data-stu-id="99a0f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99a0f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99a0f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="99a0f-121"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99a0f-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="99a0f-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99a0f-122">Library</span></span><br/> | <dl> <span data-ttu-id="99a0f-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="99a0f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99a0f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="99a0f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99a0f-125">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="99a0f-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




