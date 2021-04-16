---
description: El método IsUsingDefaultDestination determina si el representador usa la ventana de destino predeterminada.
ms.assetid: 0b956575-4cf0-4f1f-9223-bb1ec3ae8b10
title: Método CBaseControlVideo. IsUsingDefaultDestination (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultDestination
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88168442cf741e5997c2b66fc4b83bf8205e694f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671261"
---
# <a name="cbasecontrolvideoisusingdefaultdestination-method"></a><span data-ttu-id="a8307-103">CBaseControlVideo. IsUsingDefaultDestination, método</span><span class="sxs-lookup"><span data-stu-id="a8307-103">CBaseControlVideo.IsUsingDefaultDestination method</span></span>

<span data-ttu-id="a8307-104">El `IsUsingDefaultDestination` método determina si el representador utiliza la ventana de destino predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a8307-104">The `IsUsingDefaultDestination` method determines if the renderer is using the default destination window.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8307-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8307-105">Syntax</span></span>


```C++
virtual HRESULT IsUsingDefaultDestination() = 0;
```



## <a name="parameters"></a><span data-ttu-id="a8307-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8307-106">Parameters</span></span>

<span data-ttu-id="a8307-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a8307-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8307-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8307-108">Return value</span></span>

<span data-ttu-id="a8307-109">Devuelve S \_ correcto si se usa el destino predeterminado; de lo contrario, devuelve s \_ false.</span><span class="sxs-lookup"><span data-stu-id="a8307-109">Returns S\_OK if using the default destination; otherwise, returns S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8307-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8307-110">Requirements</span></span>



| <span data-ttu-id="a8307-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8307-111">Requirement</span></span> | <span data-ttu-id="a8307-112">Value</span><span class="sxs-lookup"><span data-stu-id="a8307-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8307-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8307-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a8307-114"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8307-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a8307-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8307-115">Library</span></span><br/> | <dl> <span data-ttu-id="a8307-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a8307-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8307-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8307-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8307-118">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="a8307-118">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




