---
description: Método de constructor.
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Constructor CMediaEvent. CMediaEvent (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77b87fa589728592874b0dea96f7b6efca501471
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670836"
---
# <a name="cmediaeventcmediaevent-constructor"></a><span data-ttu-id="7267c-103">Constructor CMediaEvent. CMediaEvent</span><span class="sxs-lookup"><span data-stu-id="7267c-103">CMediaEvent.CMediaEvent constructor</span></span>

<span data-ttu-id="7267c-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="7267c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7267c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7267c-105">Syntax</span></span>


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="7267c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7267c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7267c-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="7267c-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="7267c-108">Puntero al nombre del objeto para la depuración.</span><span class="sxs-lookup"><span data-stu-id="7267c-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="7267c-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="7267c-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="7267c-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="7267c-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7267c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7267c-111">Remarks</span></span>

<span data-ttu-id="7267c-112">Asigne el parámetro *pName* en la memoria estática.</span><span class="sxs-lookup"><span data-stu-id="7267c-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="7267c-113">Este nombre aparece en el terminal de depuración al crear y eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="7267c-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7267c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7267c-114">Requirements</span></span>



| <span data-ttu-id="7267c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7267c-115">Requirement</span></span> | <span data-ttu-id="7267c-116">Value</span><span class="sxs-lookup"><span data-stu-id="7267c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7267c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7267c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7267c-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7267c-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7267c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7267c-119">Library</span></span><br/> | <dl> <span data-ttu-id="7267c-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7267c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7267c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7267c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7267c-122">**Clase CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="7267c-122">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




