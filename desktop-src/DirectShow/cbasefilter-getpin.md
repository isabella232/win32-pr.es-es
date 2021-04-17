---
description: El método GetPin recupera un PIN. La clase CEnumPins llama a este método para enumerar los PIN del filtro.
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: Método CBaseFilter. GetPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660712"
---
# <a name="cbasefiltergetpin-method"></a><span data-ttu-id="fcde0-104">CBaseFilter. GetPin, método</span><span class="sxs-lookup"><span data-stu-id="fcde0-104">CBaseFilter.GetPin method</span></span>

<span data-ttu-id="fcde0-105">El método **GetPin** recupera un PIN.</span><span class="sxs-lookup"><span data-stu-id="fcde0-105">The **GetPin** method retrieves a pin.</span></span> <span data-ttu-id="fcde0-106">La clase [**CEnumPins**](cenumpins.md) llama a este método para enumerar los PIN del filtro.</span><span class="sxs-lookup"><span data-stu-id="fcde0-106">The [**CEnumPins**](cenumpins.md) class calls this method to enumerate pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcde0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcde0-107">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="fcde0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcde0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcde0-109">*n*</span><span class="sxs-lookup"><span data-stu-id="fcde0-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="fcde0-110">Índice de base cero del PIN.</span><span class="sxs-lookup"><span data-stu-id="fcde0-110">The zero-based index of the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcde0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcde0-111">Return value</span></span>

<span data-ttu-id="fcde0-112">Devuelve un puntero al objeto [**CBasePin**](cbasepin.md) que implementa el código PIN.</span><span class="sxs-lookup"><span data-stu-id="fcde0-112">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcde0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcde0-113">Remarks</span></span>

<span data-ttu-id="fcde0-114">Debe implementar este método virtual puro en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="fcde0-114">You must implement this pure virtual method in your derived class.</span></span> <span data-ttu-id="fcde0-115">Devuelve un puntero al *n* pines en este filtro, indizado desde cero.</span><span class="sxs-lookup"><span data-stu-id="fcde0-115">Return a pointer to the *n* th pin on this filter, indexed from zero.</span></span> <span data-ttu-id="fcde0-116">Puede elegir un orden de indexación arbitrario, siempre que el orden sea fijo.</span><span class="sxs-lookup"><span data-stu-id="fcde0-116">You can choose an arbitrary indexing order, as long as the ordering is fixed.</span></span> <span data-ttu-id="fcde0-117">Si el filtro agrega o elimina PIN o la ordenación cambia por algún otro motivo en tiempo de ejecución, llame al método [**CBaseFilter:: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="fcde0-117">If the filter adds or deletes pins, or the ordering changes for some other reason at run time, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcde0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcde0-118">Requirements</span></span>



| <span data-ttu-id="fcde0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcde0-119">Requirement</span></span> | <span data-ttu-id="fcde0-120">Value</span><span class="sxs-lookup"><span data-stu-id="fcde0-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcde0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcde0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fcde0-122"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcde0-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fcde0-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fcde0-123">Library</span></span><br/> | <dl> <span data-ttu-id="fcde0-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fcde0-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcde0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcde0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcde0-126">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="fcde0-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




