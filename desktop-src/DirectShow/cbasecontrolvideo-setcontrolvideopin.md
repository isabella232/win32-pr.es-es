---
description: El método SetControlVideoPin establece el PIN usado por el filtro.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Método CBaseControlVideo. SetControlVideoPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4cf47469800a4d1ecd8abe373d6f3c1fd53ece5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660261"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a><span data-ttu-id="f15b1-103">CBaseControlVideo. SetControlVideoPin, método</span><span class="sxs-lookup"><span data-stu-id="f15b1-103">CBaseControlVideo.SetControlVideoPin method</span></span>

<span data-ttu-id="f15b1-104">El `SetControlVideoPin` método establece el PIN utilizado por el filtro.</span><span class="sxs-lookup"><span data-stu-id="f15b1-104">The `SetControlVideoPin` method sets the pin used by the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f15b1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f15b1-105">Syntax</span></span>


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="f15b1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f15b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f15b1-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="f15b1-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="f15b1-108">Puntero al pin con el que se sincroniza la interfaz.</span><span class="sxs-lookup"><span data-stu-id="f15b1-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f15b1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f15b1-109">Return value</span></span>

<span data-ttu-id="f15b1-110">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f15b1-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f15b1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f15b1-111">Remarks</span></span>

<span data-ttu-id="f15b1-112">Solo se puede llamar a la interfaz cuando el filtro se ha conectado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f15b1-112">The interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="f15b1-113">El objeto se pasa a través de este método al código PIN con el que está sincronizado; en la mayoría de los casos, determinará si el PIN está conectado cuando tenga un método de interfaz llamado y devolverá VFW \_ E \_ no \_ conectado si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f15b1-113">The object is passed through this method to the pin with which it is synchronized; in most cases it will determine if the pin is connected when it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="f15b1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f15b1-114">Requirements</span></span>



| <span data-ttu-id="f15b1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f15b1-115">Requirement</span></span> | <span data-ttu-id="f15b1-116">Value</span><span class="sxs-lookup"><span data-stu-id="f15b1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f15b1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f15b1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f15b1-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f15b1-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f15b1-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f15b1-119">Library</span></span><br/> | <dl> <span data-ttu-id="f15b1-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f15b1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f15b1-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f15b1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f15b1-122">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="f15b1-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




