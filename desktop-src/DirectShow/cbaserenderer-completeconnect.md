---
description: El método CompleteConnect completa la conexión del PIN de entrada con otro PIN.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Método CBaseRenderer. CompleteConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9d2d35f99a3b3b8dc5b668b8ee9a9f94f0a53dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660757"
---
# <a name="cbaserenderercompleteconnect-method"></a><span data-ttu-id="56bc8-103">CBaseRenderer. CompleteConnect, método</span><span class="sxs-lookup"><span data-stu-id="56bc8-103">CBaseRenderer.CompleteConnect method</span></span>

<span data-ttu-id="56bc8-104">El `CompleteConnect` método completa la conexión del PIN de entrada con otro PIN.</span><span class="sxs-lookup"><span data-stu-id="56bc8-104">The `CompleteConnect` method completes the input pin's connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="56bc8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56bc8-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="56bc8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56bc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56bc8-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="56bc8-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="56bc8-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="56bc8-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56bc8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56bc8-109">Return value</span></span>

<span data-ttu-id="56bc8-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="56bc8-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="56bc8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56bc8-111">Remarks</span></span>

<span data-ttu-id="56bc8-112">El PIN de entrada del filtro llama a este método desde dentro de su propio `CompleteConnect` método, al que se llama para completar una conexión del PIN.</span><span class="sxs-lookup"><span data-stu-id="56bc8-112">The filter's input pin calls this method from inside its own `CompleteConnect` method, which is called in order to complete a pin connection.</span></span> <span data-ttu-id="56bc8-113">(Para obtener más información, vea [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md)). El filtro llama al método [**CBaseRenderer:: SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) para habilitar los eventos de [**\_ Repaint de EC**](ec-repaint.md) .</span><span class="sxs-lookup"><span data-stu-id="56bc8-113">(For more information, see [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md).) The filter calls the [**CBaseRenderer::SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) method to enable [**EC\_REPAINT**](ec-repaint.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="56bc8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56bc8-114">Requirements</span></span>



| <span data-ttu-id="56bc8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="56bc8-115">Requirement</span></span> | <span data-ttu-id="56bc8-116">Value</span><span class="sxs-lookup"><span data-stu-id="56bc8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56bc8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56bc8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="56bc8-118"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56bc8-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="56bc8-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56bc8-119">Library</span></span><br/> | <dl> <span data-ttu-id="56bc8-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="56bc8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56bc8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="56bc8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56bc8-122">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="56bc8-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




