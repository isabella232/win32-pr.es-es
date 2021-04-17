---
description: 'El método QueryPinInfo recupera información sobre el código PIN. Este método implementa el método IPin:: QueryPinInfo.'
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Método CBasePin. QueryPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670873"
---
# <a name="cbasepinquerypininfo-method"></a><span data-ttu-id="d14a0-104">CBasePin. QueryPinInfo, método</span><span class="sxs-lookup"><span data-stu-id="d14a0-104">CBasePin.QueryPinInfo method</span></span>

<span data-ttu-id="d14a0-105">El `QueryPinInfo` método recupera información sobre el código PIN.</span><span class="sxs-lookup"><span data-stu-id="d14a0-105">The `QueryPinInfo` method retrieves information about the pin.</span></span> <span data-ttu-id="d14a0-106">Este método implementa el método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="d14a0-106">This method implements the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d14a0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d14a0-107">Syntax</span></span>


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d14a0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d14a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d14a0-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="d14a0-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="d14a0-110">Puntero a una estructura de [**\_ información del PIN**](/windows/win32/api/strmif/ns-strmif-pin_info) que recibe la información del PIN.</span><span class="sxs-lookup"><span data-stu-id="d14a0-110">Pointer to a [**PIN\_INFO**](/windows/win32/api/strmif/ns-strmif-pin_info) structure that receives the pin information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d14a0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d14a0-111">Return value</span></span>

<span data-ttu-id="d14a0-112">Devuelve el \_ puntero S o E \_ .</span><span class="sxs-lookup"><span data-stu-id="d14a0-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="d14a0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d14a0-113">Remarks</span></span>

<span data-ttu-id="d14a0-114">Este método usa la variable miembro [**CBasePin:: m \_ pName**](cbasepin-m-pname.md) para el miembro **achName** de la estructura de información del PIN \_ .</span><span class="sxs-lookup"><span data-stu-id="d14a0-114">This method uses the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable for the **achName** member of the PIN\_INFO structure.</span></span>

<span data-ttu-id="d14a0-115">Cuando el método devuelve un valor, si el miembro **pFilter** de la estructura de información del PIN \_ no es **null**, tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="d14a0-115">When the method returns, if the **pFilter** member of the PIN\_INFO structure is non-**NULL**, it has an outstanding reference count.</span></span> <span data-ttu-id="d14a0-116">Cuando haya terminado, asegúrese de liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="d14a0-116">Be sure to release the interface when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="d14a0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d14a0-117">Requirements</span></span>



| <span data-ttu-id="d14a0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d14a0-118">Requirement</span></span> | <span data-ttu-id="d14a0-119">Value</span><span class="sxs-lookup"><span data-stu-id="d14a0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d14a0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d14a0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d14a0-121"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d14a0-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d14a0-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d14a0-122">Library</span></span><br/> | <dl> <span data-ttu-id="d14a0-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d14a0-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d14a0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d14a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d14a0-125">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="d14a0-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




