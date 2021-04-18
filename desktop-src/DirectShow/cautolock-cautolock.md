---
description: Método de constructor. El constructor bloquea el objeto de sección crítica especificado.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Constructor CAutoLock. CAutoLock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670822"
---
# <a name="cautolockcautolock-constructor"></a><span data-ttu-id="0b4d1-104">Constructor CAutoLock. CAutoLock</span><span class="sxs-lookup"><span data-stu-id="0b4d1-104">CAutoLock.CAutoLock constructor</span></span>

<span data-ttu-id="0b4d1-105">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="0b4d1-105">Constructor method.</span></span> <span data-ttu-id="0b4d1-106">El constructor bloquea el objeto de sección crítica especificado.</span><span class="sxs-lookup"><span data-stu-id="0b4d1-106">The constructor locks the specified critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b4d1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b4d1-107">Syntax</span></span>


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a><span data-ttu-id="0b4d1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b4d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b4d1-109">*plock*</span><span class="sxs-lookup"><span data-stu-id="0b4d1-109">*plock*</span></span> 
</dt> <dd>

<span data-ttu-id="0b4d1-110">Puntero a un objeto [**CCritSec**](ccritsec.md) , que contiene un objeto de sección crítica.</span><span class="sxs-lookup"><span data-stu-id="0b4d1-110">Pointer to a [**CCritSec**](ccritsec.md) object, which contains a critical section object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b4d1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b4d1-111">Requirements</span></span>



| <span data-ttu-id="0b4d1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b4d1-112">Requirement</span></span> | <span data-ttu-id="0b4d1-113">Value</span><span class="sxs-lookup"><span data-stu-id="0b4d1-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4d1-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b4d1-114">Header</span></span><br/>  | <dl> <span data-ttu-id="0b4d1-115"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b4d1-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0b4d1-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b4d1-116">Library</span></span><br/> | <dl> <span data-ttu-id="0b4d1-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0b4d1-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b4d1-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b4d1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b4d1-119">**Clase CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="0b4d1-119">**CAutoLock Class**</span></span>](cautolock.md)
</dt> </dl>

 

 




