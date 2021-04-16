---
description: El método de vaciado notifica a la clase base que el PIN se ha iniciado o detenido el vaciado.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: CBaseStreamControl. Flush (método) (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671283"
---
# <a name="cbasestreamcontrolflushing-method"></a><span data-ttu-id="b4489-103">CBaseStreamControl. Flush (método)</span><span class="sxs-lookup"><span data-stu-id="b4489-103">CBaseStreamControl.Flushing method</span></span>

<span data-ttu-id="b4489-104">El `Flushing` método notifica a la clase base que el PIN se ha iniciado o detenido.</span><span class="sxs-lookup"><span data-stu-id="b4489-104">The `Flushing` method notifies the base class that the pin has started or stopped flushing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4489-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4489-105">Syntax</span></span>


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a><span data-ttu-id="b4489-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4489-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4489-107">*bInProgress*</span><span class="sxs-lookup"><span data-stu-id="b4489-107">*bInProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="b4489-108">Especifica un valor booleano que indica si el PIN se está vaciando.</span><span class="sxs-lookup"><span data-stu-id="b4489-108">Specifies a Boolean value that indicates whether the pin is flushing.</span></span> <span data-ttu-id="b4489-109">Use el valor **true** cuando el PIN comienza una operación de vaciado y **false** cuando el PIN finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="b4489-109">Use the value **TRUE** when the pin begins a flush operation, and **FALSE** when the pin ends a flush operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4489-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4489-110">Return value</span></span>

<span data-ttu-id="b4489-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b4489-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4489-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4489-112">Remarks</span></span>

<span data-ttu-id="b4489-113">El PIN debe llamar a este método desde sus métodos [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) y [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="b4489-113">The pin must call this method from within its [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span> <span data-ttu-id="b4489-114">Especifique **true** en **BeginFlush** y **false** en **EndFlush**.</span><span class="sxs-lookup"><span data-stu-id="b4489-114">Specify **TRUE** in **BeginFlush** and **FALSE** in **EndFlush**.</span></span>

<span data-ttu-id="b4489-115">Este método hace que el método [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) deje de esperar.</span><span class="sxs-lookup"><span data-stu-id="b4489-115">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="b4489-116">Mientras se está vaciando el PIN, **CheckStreamState** siempre devuelve el \_ descartado de la transmisión.</span><span class="sxs-lookup"><span data-stu-id="b4489-116">While the pin is flushing, **CheckStreamState** always returns STREAM\_DISCARDING.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4489-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4489-117">Requirements</span></span>



| <span data-ttu-id="b4489-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4489-118">Requirement</span></span> | <span data-ttu-id="b4489-119">Value</span><span class="sxs-lookup"><span data-stu-id="b4489-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4489-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4489-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b4489-121"><dt>Strmctl. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4489-121"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b4489-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4489-122">Library</span></span><br/> | <dl> <span data-ttu-id="b4489-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b4489-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4489-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4489-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4489-125">**Clase CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="b4489-125">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




