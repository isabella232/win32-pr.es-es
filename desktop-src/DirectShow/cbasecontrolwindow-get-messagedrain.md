---
description: El \_ método get MessageDrain recupera la purga del mensaje actual.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: Método CBaseControlWindow.get_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660346"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a><span data-ttu-id="e68c0-103">CBaseControlWindow. Get \_ MessageDrain (método)</span><span class="sxs-lookup"><span data-stu-id="e68c0-103">CBaseControlWindow.get\_MessageDrain method</span></span>

<span data-ttu-id="e68c0-104">El `get_MessageDrain` método recupera la purga del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="e68c0-104">The `get_MessageDrain` method retrieves the current message drain.</span></span>

## <a name="syntax"></a><span data-ttu-id="e68c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e68c0-105">Syntax</span></span>


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a><span data-ttu-id="e68c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e68c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e68c0-107">*Purga*</span><span class="sxs-lookup"><span data-stu-id="e68c0-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="e68c0-108">Puntero a la ventana actual que recibe los mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="e68c0-108">Pointer to the current window receiving window messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e68c0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e68c0-109">Return value</span></span>

<span data-ttu-id="e68c0-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e68c0-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e68c0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e68c0-111">Remarks</span></span>

<span data-ttu-id="e68c0-112">Los mensajes enviados al filtro de representador de vídeo se pueden publicar en otra ventana.</span><span class="sxs-lookup"><span data-stu-id="e68c0-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="e68c0-113">La ventana registrada para recibir estos mensajes (mediante la función miembro **CBaseControlWindow:: get \_ MessageDrain** ) es la purga del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="e68c0-113">The window registered to receive these messages (using the **CBaseControlWindow::get\_MessageDrain** member function) is the current message drain.</span></span>

## <a name="requirements"></a><span data-ttu-id="e68c0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e68c0-114">Requirements</span></span>



| <span data-ttu-id="e68c0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e68c0-115">Requirement</span></span> | <span data-ttu-id="e68c0-116">Value</span><span class="sxs-lookup"><span data-stu-id="e68c0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e68c0-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e68c0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e68c0-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e68c0-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e68c0-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e68c0-119">Library</span></span><br/> | <dl> <span data-ttu-id="e68c0-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e68c0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e68c0-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e68c0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e68c0-122">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="e68c0-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




