---
description: El método AddHead inserta otra lista al principio de esta lista.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Método CBaseList. AddHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a262f2bcfb7c40671fd472ecd7d3f887b1db4224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670943"
---
# <a name="cbaselistaddhead-method"></a><span data-ttu-id="3c8f0-103">CBaseList. AddHead, método</span><span class="sxs-lookup"><span data-stu-id="3c8f0-103">CBaseList.AddHead method</span></span>

<span data-ttu-id="3c8f0-104">El `AddHead` método inserta otra lista al principio de esta lista.</span><span class="sxs-lookup"><span data-stu-id="3c8f0-104">The `AddHead` method inserts another list at the front of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c8f0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c8f0-105">Syntax</span></span>


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="3c8f0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c8f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c8f0-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="3c8f0-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="3c8f0-108">Puntero a la lista de elementos que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="3c8f0-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c8f0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c8f0-109">Return value</span></span>

<span data-ttu-id="3c8f0-110">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3c8f0-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c8f0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c8f0-111">Remarks</span></span>

<span data-ttu-id="3c8f0-112">Si se produce un error en el método, es posible que algunos elementos se hayan agregado a la lista.</span><span class="sxs-lookup"><span data-stu-id="3c8f0-112">If the method fails, some items might have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c8f0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c8f0-113">Requirements</span></span>



| <span data-ttu-id="3c8f0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c8f0-114">Requirement</span></span> | <span data-ttu-id="3c8f0-115">Value</span><span class="sxs-lookup"><span data-stu-id="3c8f0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c8f0-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c8f0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3c8f0-117"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c8f0-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3c8f0-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c8f0-118">Library</span></span><br/> | <dl> <span data-ttu-id="3c8f0-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3c8f0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c8f0-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c8f0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c8f0-121">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="3c8f0-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




