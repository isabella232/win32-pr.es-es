---
description: 'Constructor DEEVENT.CAMEvent: método constructor.'
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Constructor CAMEvent.CAMEvent (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cdd37ba72d9467c16d46b2aec3ec40c206466eaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096542"
---
# <a name="cameventcamevent-constructor"></a><span data-ttu-id="fb202-103">Constructor DE EVENTOS.CAMEvent</span><span class="sxs-lookup"><span data-stu-id="fb202-103">CAMEvent.CAMEvent constructor</span></span>

<span data-ttu-id="fb202-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="fb202-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb202-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb202-105">Syntax</span></span>


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="fb202-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb202-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb202-107">*fManualReset*</span><span class="sxs-lookup"><span data-stu-id="fb202-107">*fManualReset*</span></span> 
</dt> <dd>

<span data-ttu-id="fb202-108">Valor booleano que especifica si el objeto es un evento de restablecimiento manual o un evento de restablecimiento automático.</span><span class="sxs-lookup"><span data-stu-id="fb202-108">Boolean value that specifies whether the object is a manual-reset event or an auto-reset event.</span></span> <span data-ttu-id="fb202-109">Si **es TRUE,** el objeto es un evento de restablecimiento manual.</span><span class="sxs-lookup"><span data-stu-id="fb202-109">If **TRUE**, the object is a manual-reset event.</span></span> <span data-ttu-id="fb202-110">De lo contrario, es un evento de restablecimiento automático.</span><span class="sxs-lookup"><span data-stu-id="fb202-110">Otherwise, it is an auto-reset event.</span></span>

</dd> <dt>

<span data-ttu-id="fb202-111">*Phr*</span><span class="sxs-lookup"><span data-stu-id="fb202-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="fb202-112">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="fb202-112">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="fb202-113">Si se produce un error en el constructor, este parámetro recibe un código de error.</span><span class="sxs-lookup"><span data-stu-id="fb202-113">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="fb202-114">Si esto ocurre, el objeto no está en un estado válido.</span><span class="sxs-lookup"><span data-stu-id="fb202-114">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="fb202-115">Para la compatibilidad con versiones anteriores de strmbase.lib, el valor predeterminado de este parámetro es **NULL.**</span><span class="sxs-lookup"><span data-stu-id="fb202-115">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="fb202-116">Sin embargo, se prefiere pasar un valor distinto de **NULL,** para que el autor de la llamada pueda comprobar el estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="fb202-116">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb202-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb202-117">Remarks</span></span>

<span data-ttu-id="fb202-118">El evento comienza en un estado sin signo.</span><span class="sxs-lookup"><span data-stu-id="fb202-118">The event begins in a nonsignaled state.</span></span>

<span data-ttu-id="fb202-119">Con un evento de restablecimiento automático, el método [**CAMEvent::Wait**](camevent-wait.md) restablece el evento a no firma cuando el método vuelve.</span><span class="sxs-lookup"><span data-stu-id="fb202-119">With an auto-reset event, the [**CAMEvent::Wait**](camevent-wait.md) method resets the event to nonsignaled when the method returns.</span></span> <span data-ttu-id="fb202-120">Con un evento de restablecimiento manual, el evento permanece señalado hasta que se llama al [**método CAMEvent::Reset.**](camevent-reset.md)</span><span class="sxs-lookup"><span data-stu-id="fb202-120">With a manual-reset event, the event remains signaled until you call the [**CAMEvent::Reset**](camevent-reset.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb202-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb202-121">Requirements</span></span>



| <span data-ttu-id="fb202-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb202-122">Requirement</span></span> | <span data-ttu-id="fb202-123">Value</span><span class="sxs-lookup"><span data-stu-id="fb202-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb202-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb202-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fb202-125"><dt>Wxutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb202-125"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="fb202-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb202-126">Library</span></span><br/> | <dl> <span data-ttu-id="fb202-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fb202-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb202-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fb202-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb202-129">**CLASE CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="fb202-129">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




