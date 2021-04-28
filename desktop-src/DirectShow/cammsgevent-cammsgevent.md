---
description: 'Constructor CAMMsgEvent.CAMMsgEvent: método constructor.'
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Constructor CAMMsgEvent.CAMMsgEvent (Wxutil.h)
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
ms.openlocfilehash: dac72ecb97a1ea1fd2594af9c11b8a03078cf2cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096543"
---
# <a name="cammsgeventcammsgevent-constructor"></a><span data-ttu-id="1e56c-103">Constructor CAMMsgEvent.CAMMsgEvent</span><span class="sxs-lookup"><span data-stu-id="1e56c-103">CAMMsgEvent.CAMMsgEvent constructor</span></span>

<span data-ttu-id="1e56c-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="1e56c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e56c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e56c-105">Syntax</span></span>


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="1e56c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e56c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e56c-107">*Phr*</span><span class="sxs-lookup"><span data-stu-id="1e56c-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1e56c-108">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="1e56c-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="1e56c-109">Si se produce un error en el constructor, este parámetro recibe un código de error.</span><span class="sxs-lookup"><span data-stu-id="1e56c-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="1e56c-110">Si esto ocurre, el objeto no está en un estado válido.</span><span class="sxs-lookup"><span data-stu-id="1e56c-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="1e56c-111">Para la compatibilidad con versiones anteriores de strmbase.lib, este parámetro tiene como valor predeterminado **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1e56c-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="1e56c-112">Sin embargo, se prefiere pasar un valor distinto de **NULL,** para que el autor de la llamada pueda comprobar el estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="1e56c-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e56c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e56c-113">Requirements</span></span>



| <span data-ttu-id="1e56c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e56c-114">Requirement</span></span> | <span data-ttu-id="1e56c-115">Value</span><span class="sxs-lookup"><span data-stu-id="1e56c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e56c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e56c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1e56c-117"><dt>Wxutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e56c-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1e56c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e56c-118">Library</span></span><br/> | <dl> <span data-ttu-id="1e56c-119"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1e56c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e56c-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1e56c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e56c-121">**CLASE CAMMsgEvent**</span><span class="sxs-lookup"><span data-stu-id="1e56c-121">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




