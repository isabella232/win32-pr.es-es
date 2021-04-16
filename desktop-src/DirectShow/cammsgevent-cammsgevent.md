---
description: Método de constructor.
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Constructor CAMMsgEvent. CAMMsgEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d207afae53a715728d8307656b0c2427ce9574c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671623"
---
# <a name="cammsgeventcammsgevent-constructor"></a><span data-ttu-id="2c0e0-103">Constructor CAMMsgEvent. CAMMsgEvent</span><span class="sxs-lookup"><span data-stu-id="2c0e0-103">CAMMsgEvent.CAMMsgEvent constructor</span></span>

<span data-ttu-id="2c0e0-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c0e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c0e0-105">Syntax</span></span>


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="2c0e0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c0e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c0e0-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="2c0e0-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="2c0e0-108">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2c0e0-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="2c0e0-109">Si se produce un error en el constructor, este parámetro recibe un código de error.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="2c0e0-110">Si esto ocurre, el objeto no tiene un estado válido.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="2c0e0-111">Para mantener la compatibilidad con versiones anteriores de strmbase. lib, este parámetro tiene como valor predeterminado **null**.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="2c0e0-112">Sin embargo, se prefiere pasar un valor distinto de **null** para que el autor de la llamada pueda comprobar el estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="2c0e0-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c0e0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c0e0-113">Requirements</span></span>



| <span data-ttu-id="2c0e0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c0e0-114">Requirement</span></span> | <span data-ttu-id="2c0e0-115">Value</span><span class="sxs-lookup"><span data-stu-id="2c0e0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c0e0-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c0e0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2c0e0-117"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c0e0-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2c0e0-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c0e0-118">Library</span></span><br/> | <dl> <span data-ttu-id="2c0e0-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2c0e0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c0e0-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c0e0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c0e0-121">**Clase CAMMsgEvent**</span><span class="sxs-lookup"><span data-stu-id="2c0e0-121">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




