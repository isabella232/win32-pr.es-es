---
description: El método SetControlWindowPin establece el pin con el que se va a sincronizar.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Método CBaseControlWindow. SetControlWindowPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1aa3d4960799c2286e17709258ea90b76332bc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661337"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a><span data-ttu-id="a9484-103">CBaseControlWindow. SetControlWindowPin, método</span><span class="sxs-lookup"><span data-stu-id="a9484-103">CBaseControlWindow.SetControlWindowPin method</span></span>

<span data-ttu-id="a9484-104">El `SetControlWindowPin` método establece el pin con el que se va a sincronizar.</span><span class="sxs-lookup"><span data-stu-id="a9484-104">The `SetControlWindowPin` method sets the pin with which to synchronize.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9484-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9484-105">Syntax</span></span>


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="a9484-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9484-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9484-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="a9484-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a9484-108">Puntero al pin con el que se sincroniza la interfaz.</span><span class="sxs-lookup"><span data-stu-id="a9484-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9484-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9484-109">Return value</span></span>

<span data-ttu-id="a9484-110">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a9484-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9484-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9484-111">Remarks</span></span>

<span data-ttu-id="a9484-112">Esta función miembro establece la \_ variable miembro m pPin igual que el parámetro pPin.</span><span class="sxs-lookup"><span data-stu-id="a9484-112">This member function sets the m\_pPin member variable equal to the pPin parameter.</span></span> <span data-ttu-id="a9484-113">Tal y como se describe en el constructor, solo se puede llamar a la interfaz cuando el filtro se ha conectado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a9484-113">As described in the constructor, the interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="a9484-114">El objeto se pasa a través de esta función miembro al pin con el que se debe sincronizar; en la mayoría de los casos, determinará si el PIN está conectado siempre que tenga un método de interfaz llamado y devolverá VFW \_ E \_ no \_ conectado si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a9484-114">The object is passed in through this member function to the pin with which it should synchronize; in most cases, it will determine if the pin is connected whenever it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9484-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9484-115">Requirements</span></span>



| <span data-ttu-id="a9484-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9484-116">Requirement</span></span> | <span data-ttu-id="a9484-117">Value</span><span class="sxs-lookup"><span data-stu-id="a9484-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9484-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9484-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a9484-119"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9484-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a9484-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a9484-120">Library</span></span><br/> | <dl> <span data-ttu-id="a9484-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a9484-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9484-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9484-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9484-123">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="a9484-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




