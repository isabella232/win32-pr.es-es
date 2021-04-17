---
description: 'El método EndOfStream notifica al pin que no se espera ningún dato adicional, hasta que se emite un nuevo comando de ejecución para el filtro. Este método implementa el método IPin:: EndOfStream.'
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Método CRenderedInputPin. EndOfStream (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c836b1098c92a69fa720fb7b87e4a63b3c05a526
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660746"
---
# <a name="crenderedinputpinendofstream-method"></a><span data-ttu-id="0510e-104">CRenderedInputPin. EndOfStream, método</span><span class="sxs-lookup"><span data-stu-id="0510e-104">CRenderedInputPin.EndOfStream method</span></span>

<span data-ttu-id="0510e-105">El `EndOfStream` método notifica al pin que no se espera ningún dato adicional, hasta que se emite un nuevo comando de ejecución para el filtro.</span><span class="sxs-lookup"><span data-stu-id="0510e-105">The `EndOfStream` method notifies the pin that no additional data is expected, until a new run command is issued to the filter.</span></span> <span data-ttu-id="0510e-106">Este método implementa el método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="0510e-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0510e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0510e-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="0510e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0510e-108">Parameters</span></span>

<span data-ttu-id="0510e-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0510e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0510e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0510e-110">Return value</span></span>

<span data-ttu-id="0510e-111">Devuelve \_ si es correcto, o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0510e-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0510e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0510e-112">Remarks</span></span>

<span data-ttu-id="0510e-113">Si el filtro se está ejecutando, este método envía un evento [**EC \_ Complete**](ec-complete.md) al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="0510e-113">If the filter is running, this method sends an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> <span data-ttu-id="0510e-114">De lo contrario, se establece una marca para que el \_ evento de finalización de EC se envíe cuando se ejecute el filtro siguiente.</span><span class="sxs-lookup"><span data-stu-id="0510e-114">Otherwise, is sets a flag so that the EC\_COMPLETE event is sent when the filter next runs.</span></span> <span data-ttu-id="0510e-115">Vaciar el filtro borra la marca.</span><span class="sxs-lookup"><span data-stu-id="0510e-115">Flushing the filter clears the flag.</span></span>

<span data-ttu-id="0510e-116">Debe invalidar este método para que contenga el bloqueo de streaming del PIN:</span><span class="sxs-lookup"><span data-stu-id="0510e-116">You should override this method to hold the pin's streaming lock:</span></span>


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



<span data-ttu-id="0510e-117">Además, si el filtro procesa llamadas de **recepción** de forma asincrónica, el PIN debe esperar para enviar el \_ evento de finalización de EC hasta que el filtro haya procesado todos los ejemplos pendientes.</span><span class="sxs-lookup"><span data-stu-id="0510e-117">Also, if the filter processes **Receive** calls asynchronously, the pin should wait to send the EC\_COMPLETE event until the filter has processed all pending samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="0510e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0510e-118">Requirements</span></span>



| <span data-ttu-id="0510e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0510e-119">Requirement</span></span> | <span data-ttu-id="0510e-120">Value</span><span class="sxs-lookup"><span data-stu-id="0510e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0510e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0510e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0510e-122"><dt>Amextra. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0510e-122"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0510e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0510e-123">Library</span></span><br/> | <dl> <span data-ttu-id="0510e-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0510e-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0510e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0510e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0510e-126">**Clase CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="0510e-126">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




