---
description: 'El método StopAt informa al pin Cuándo detener la entrega de datos. Este método implementa el método IAMStreamControl:: StopAt.'
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: Método CBaseStreamControl. StopAt (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678890"
---
# <a name="cbasestreamcontrolstopat-method"></a><span data-ttu-id="e940a-104">CBaseStreamControl. StopAt, método</span><span class="sxs-lookup"><span data-stu-id="e940a-104">CBaseStreamControl.StopAt method</span></span>

<span data-ttu-id="e940a-105">El `StopAt` método informa al pin Cuándo detener la entrega de datos.</span><span class="sxs-lookup"><span data-stu-id="e940a-105">The `StopAt` method informs the pin when to stop delivering data.</span></span> <span data-ttu-id="e940a-106">Este método implementa el método [**IAMStreamControl:: StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="e940a-106">This method implements the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e940a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e940a-107">Syntax</span></span>


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="e940a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e940a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e940a-109">*ptStop*</span><span class="sxs-lookup"><span data-stu-id="e940a-109">*ptStop*</span></span> 
</dt> <dd>

<span data-ttu-id="e940a-110">Puntero a un valor de [**\_ hora de referencia**](reference-time.md) que especifica cuando el PIN debe dejar de entregar datos.</span><span class="sxs-lookup"><span data-stu-id="e940a-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should stop delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="e940a-111">*bSendExtra*</span><span class="sxs-lookup"><span data-stu-id="e940a-111">*bSendExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="e940a-112">Especifica un valor booleano que indica si se va a enviar un ejemplo adicional después de la hora de detención programada.</span><span class="sxs-lookup"><span data-stu-id="e940a-112">Specifies a Boolean value that indicates whether to send an extra sample after the scheduled stop time.</span></span> <span data-ttu-id="e940a-113">Si **es true**, el PIN envía un ejemplo adicional.</span><span class="sxs-lookup"><span data-stu-id="e940a-113">If **TRUE**, the pin sends one extra sample.</span></span>

</dd> <dt>

<span data-ttu-id="e940a-114">*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="e940a-114">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="e940a-115">Especifica un valor que se enviará junto con la notificación de inicio.</span><span class="sxs-lookup"><span data-stu-id="e940a-115">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e940a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e940a-116">Return value</span></span>

<span data-ttu-id="e940a-117">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="e940a-117">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="e940a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e940a-118">Requirements</span></span>



| <span data-ttu-id="e940a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e940a-119">Requirement</span></span> | <span data-ttu-id="e940a-120">Value</span><span class="sxs-lookup"><span data-stu-id="e940a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e940a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e940a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e940a-122"><dt>Strmctl. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e940a-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e940a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e940a-123">Library</span></span><br/> | <dl> <span data-ttu-id="e940a-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e940a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e940a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e940a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e940a-126">**Clase CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="e940a-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




