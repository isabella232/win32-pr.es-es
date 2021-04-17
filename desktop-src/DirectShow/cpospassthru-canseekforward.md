---
description: 'El método CanSeekForward determina si se puede buscar en el flujo hacia delante. Este método implementa el método IMediaPosition:: CanSeekForward.'
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: Método CPosPassThru. CanSeekForward (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 701bfdff1d3a3a37dc0e3935aa82bfca2e01cfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680475"
---
# <a name="cpospassthrucanseekforward-method"></a><span data-ttu-id="689a1-104">CPosPassThru. CanSeekForward, método</span><span class="sxs-lookup"><span data-stu-id="689a1-104">CPosPassThru.CanSeekForward method</span></span>

<span data-ttu-id="689a1-105">El `CanSeekForward` método determina si se puede buscar en el flujo hacia delante.</span><span class="sxs-lookup"><span data-stu-id="689a1-105">The `CanSeekForward` method determines whether the stream can be seeked forward.</span></span> <span data-ttu-id="689a1-106">Este método implementa el método [**IMediaPosition:: CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) .</span><span class="sxs-lookup"><span data-stu-id="689a1-106">This method implements the [**IMediaPosition::CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="689a1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="689a1-107">Syntax</span></span>


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a><span data-ttu-id="689a1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="689a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="689a1-109">*pCanSeekForward*</span><span class="sxs-lookup"><span data-stu-id="689a1-109">*pCanSeekForward*</span></span> 
</dt> <dd>

<span data-ttu-id="689a1-110">Puntero a una variable que recibe el valor OATRUE si el filtro puede buscar hacia delante o OAFALSE de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="689a1-110">Pointer to a variable that receives the value OATRUE if the filter can seek forward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="689a1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="689a1-111">Return value</span></span>

<span data-ttu-id="689a1-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="689a1-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="689a1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="689a1-113">Requirements</span></span>



| <span data-ttu-id="689a1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="689a1-114">Requirement</span></span> | <span data-ttu-id="689a1-115">Value</span><span class="sxs-lookup"><span data-stu-id="689a1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="689a1-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="689a1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="689a1-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="689a1-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="689a1-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="689a1-118">Library</span></span><br/> | <dl> <span data-ttu-id="689a1-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="689a1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="689a1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="689a1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="689a1-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="689a1-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




