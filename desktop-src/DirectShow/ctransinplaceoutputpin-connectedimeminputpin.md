---
description: 'El método ConnectedIMemInputPin recupera un puntero al pin de entrada de nivel inferior. Este método devuelve la variable miembro CBaseOutputPin:: m \_ pInputPin.'
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Método CTransInPlaceOutputPin. ConnectedIMemInputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660359"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a><span data-ttu-id="7c1a1-104">CTransInPlaceOutputPin. ConnectedIMemInputPin, método</span><span class="sxs-lookup"><span data-stu-id="7c1a1-104">CTransInPlaceOutputPin.ConnectedIMemInputPin method</span></span>

<span data-ttu-id="7c1a1-105">El `ConnectedIMemInputPin` método recupera un puntero al pin de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="7c1a1-105">The `ConnectedIMemInputPin` method retrieves a pointer to the downstream input pin.</span></span> <span data-ttu-id="7c1a1-106">Este método devuelve la variable miembro [**CBaseOutputPin:: m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1a1-106">This method returns the [**CBaseOutputPin::m\_pInputPin**](cbaseoutputpin-m-pinputpin.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c1a1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c1a1-107">Syntax</span></span>


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a><span data-ttu-id="7c1a1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c1a1-108">Parameters</span></span>

<span data-ttu-id="7c1a1-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7c1a1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c1a1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c1a1-110">Return value</span></span>

<span data-ttu-id="7c1a1-111">Devuelve un puntero a la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) en el PIN de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="7c1a1-111">Returns a pointer to the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c1a1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c1a1-112">Requirements</span></span>



| <span data-ttu-id="7c1a1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c1a1-113">Requirement</span></span> | <span data-ttu-id="7c1a1-114">Value</span><span class="sxs-lookup"><span data-stu-id="7c1a1-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c1a1-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c1a1-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7c1a1-116"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a1-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7c1a1-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c1a1-117">Library</span></span><br/> | <dl> <span data-ttu-id="7c1a1-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a1-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c1a1-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c1a1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c1a1-120">**Clase CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="7c1a1-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




