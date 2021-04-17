---
description: Devuelve FALSE si el subproceso actual es el propietario de la sección crítica especificada.
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: Función CritCheckOut (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670725"
---
# <a name="critcheckout-function"></a><span data-ttu-id="33963-103">CritCheckOut función)</span><span class="sxs-lookup"><span data-stu-id="33963-103">CritCheckOut function</span></span>

<span data-ttu-id="33963-104">Devuelve **false** si el subproceso actual es el propietario de la sección crítica especificada.</span><span class="sxs-lookup"><span data-stu-id="33963-104">Returns **FALSE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="33963-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33963-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="33963-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33963-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33963-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="33963-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="33963-108">Puntero a una sección crítica de [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="33963-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33963-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33963-109">Return value</span></span>

<span data-ttu-id="33963-110">En las compilaciones de depuración, devuelve **false** si el subproceso actual es el propietario de esta sección crítica, o bien **true** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="33963-110">In debug builds, returns **FALSE** if the current thread is the owner of this critical section, or **TRUE** otherwise.</span></span> <span data-ttu-id="33963-111">En las compilaciones comerciales, siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="33963-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="33963-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33963-112">Remarks</span></span>

<span data-ttu-id="33963-113">Esta función es la inversa de la función [**CritCheckIn**](critcheckin.md) .</span><span class="sxs-lookup"><span data-stu-id="33963-113">This function is the inverse of the [**CritCheckIn**](critcheckin.md) function.</span></span> <span data-ttu-id="33963-114">Si **CritCheckIn** devuelve **true**, **CritCheckOut** devuelve **false** y viceversa.</span><span class="sxs-lookup"><span data-stu-id="33963-114">If **CritCheckIn** returns **TRUE**, **CritCheckOut** returns **FALSE**, and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="33963-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33963-115">Requirements</span></span>



| <span data-ttu-id="33963-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="33963-116">Requirement</span></span> | <span data-ttu-id="33963-117">Value</span><span class="sxs-lookup"><span data-stu-id="33963-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33963-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33963-118">Header</span></span><br/>  | <dl> <span data-ttu-id="33963-119"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33963-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="33963-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33963-120">Library</span></span><br/> | <dl> <span data-ttu-id="33963-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="33963-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33963-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="33963-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33963-123">Funciones de depuración de sección crítica</span><span class="sxs-lookup"><span data-stu-id="33963-123">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




