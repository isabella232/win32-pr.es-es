---
description: 'Constructor CBaseReferenceClock.CBaseReferenceClock: método constructor.'
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Constructor CBaseReferenceClock.CBaseReferenceClock (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9840bb9d733641ada7c45b0df1470a4150b8ec85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119943"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a><span data-ttu-id="9fd40-103">Constructor CBaseReferenceClock.CBaseReferenceClock</span><span class="sxs-lookup"><span data-stu-id="9fd40-103">CBaseReferenceClock.CBaseReferenceClock constructor</span></span>

<span data-ttu-id="9fd40-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="9fd40-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fd40-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fd40-105">Syntax</span></span>


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="9fd40-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fd40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fd40-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="9fd40-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd40-108">Puntero a una cadena que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="9fd40-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="9fd40-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="9fd40-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fd40-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="9fd40-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd40-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="9fd40-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="9fd40-112">Si el objeto se agrega, pase un puntero a la interfaz IUnknown del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="9fd40-112">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="9fd40-113">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="9fd40-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9fd40-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="9fd40-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd40-115">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="9fd40-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="9fd40-116">Si se produce un error, el método devuelve un código de error en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="9fd40-116">If an error occurs, the method returns an error code in this parameter.</span></span> <span data-ttu-id="9fd40-117">No establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="9fd40-117">Do not set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9fd40-118">*pSched*</span><span class="sxs-lookup"><span data-stu-id="9fd40-118">*pSched*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd40-119">Puntero a un [**objeto CAMSchedule.**](camschedule.md)</span><span class="sxs-lookup"><span data-stu-id="9fd40-119">Pointer to a [**CAMSchedule**](camschedule.md) object.</span></span> <span data-ttu-id="9fd40-120">Si **es NULL,** este método crea un **nuevo objeto CAMSchedule.**</span><span class="sxs-lookup"><span data-stu-id="9fd40-120">If **NULL**, this method creates a new **CAMSchedule** object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9fd40-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fd40-121">Requirements</span></span>



| <span data-ttu-id="9fd40-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fd40-122">Requirement</span></span> | <span data-ttu-id="9fd40-123">Value</span><span class="sxs-lookup"><span data-stu-id="9fd40-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd40-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fd40-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9fd40-125"><dt>Refclock.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fd40-125"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9fd40-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9fd40-126">Library</span></span><br/> | <dl> <span data-ttu-id="9fd40-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9fd40-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fd40-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9fd40-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd40-129">**CBaseReferenceClock (clase)**</span><span class="sxs-lookup"><span data-stu-id="9fd40-129">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




