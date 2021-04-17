---
description: 'El método BeginFlush inicia una operación de vaciado. Implementa el método IPin:: BeginFlush.'
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Método CBaseOutputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0216f74094d0c024d9b354dc594ff8d65315efbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671110"
---
# <a name="cbaseoutputpinbeginflush-method"></a><span data-ttu-id="ea758-104">CBaseOutputPin. BeginFlush, método</span><span class="sxs-lookup"><span data-stu-id="ea758-104">CBaseOutputPin.BeginFlush method</span></span>

<span data-ttu-id="ea758-105">El `BeginFlush` método inicia una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="ea758-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="ea758-106">Implementa el método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="ea758-106">Implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea758-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea758-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="ea758-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea758-108">Parameters</span></span>

<span data-ttu-id="ea758-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ea758-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea758-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea758-110">Return value</span></span>

<span data-ttu-id="ea758-111">Devuelve E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="ea758-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea758-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea758-112">Remarks</span></span>

<span data-ttu-id="ea758-113">Solo se debe llamar a este método en los pin de entrada, por lo que la implementación de **CBaseOutputPin** devuelve E \_ inesperada.</span><span class="sxs-lookup"><span data-stu-id="ea758-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea758-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea758-114">Requirements</span></span>



| <span data-ttu-id="ea758-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea758-115">Requirement</span></span> | <span data-ttu-id="ea758-116">Value</span><span class="sxs-lookup"><span data-stu-id="ea758-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea758-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea758-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ea758-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea758-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ea758-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea758-119">Library</span></span><br/> | <dl> <span data-ttu-id="ea758-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ea758-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea758-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea758-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea758-122">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="ea758-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




