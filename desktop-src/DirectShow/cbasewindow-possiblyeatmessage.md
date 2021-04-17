---
description: El método PossiblyEatMessage permite a una clase derivada reenviar mensajes a otra ventana.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Método CBaseWindow. PossiblyEatMessage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f218b62ac5464da27b8596992c34ce7ae5efde46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660314"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a><span data-ttu-id="38ca1-103">CBaseWindow. PossiblyEatMessage, método</span><span class="sxs-lookup"><span data-stu-id="38ca1-103">CBaseWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="38ca1-104">El `PossiblyEatMessage` método permite a una clase derivada reenviar mensajes a otra ventana.</span><span class="sxs-lookup"><span data-stu-id="38ca1-104">The `PossiblyEatMessage` method enables a derived class to forward messages to another window.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ca1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38ca1-105">Syntax</span></span>


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="38ca1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38ca1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ca1-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="38ca1-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="38ca1-108">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="38ca1-108">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="38ca1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38ca1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38ca1-110">Primer parámetro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="38ca1-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="38ca1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38ca1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38ca1-112">Segundo parámetro del mensaje.</span><span class="sxs-lookup"><span data-stu-id="38ca1-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38ca1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38ca1-113">Return value</span></span>

<span data-ttu-id="38ca1-114">Devuelve **true** si el mensaje se reenvió o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="38ca1-114">Returns **TRUE** if the message was forwarded, or **FALSE** otherwise.</span></span> <span data-ttu-id="38ca1-115">La clase base devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="38ca1-115">The base class returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="38ca1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38ca1-116">Remarks</span></span>

<span data-ttu-id="38ca1-117">Antes de que el método [**CBaseWindow:: OnReceiveMessage**](cbasewindow-onreceivemessage.md) controle un mensaje, llama a `PossiblyEatMessage` .</span><span class="sxs-lookup"><span data-stu-id="38ca1-117">Before the [**CBaseWindow::OnReceiveMessage**](cbasewindow-onreceivemessage.md) method handles a message, it calls `PossiblyEatMessage`.</span></span> <span data-ttu-id="38ca1-118">Si `PossiblyEatMessage` devuelve **true**, **OnReceiveMessage** omite el mensaje.</span><span class="sxs-lookup"><span data-stu-id="38ca1-118">If `PossiblyEatMessage` returns **TRUE**, **OnReceiveMessage** ignores the message.</span></span> <span data-ttu-id="38ca1-119">Una clase derivada puede invalidar `PossiblyEatMessage` para que reenvíe algunos mensajes a una ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="38ca1-119">A derived class can override `PossiblyEatMessage` so that it forwards some messages to an owner window.</span></span> <span data-ttu-id="38ca1-120">Por ejemplo, la clase [**CBaseControlWindow**](cbasecontrolwindow.md) , que se deriva de **CBaseWindow**, reenvía los mensajes de teclado y del mouse.</span><span class="sxs-lookup"><span data-stu-id="38ca1-120">For example, the [**CBaseControlWindow**](cbasecontrolwindow.md) class, which derives from **CBaseWindow**, forwards keyboard and mouse messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="38ca1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38ca1-121">Requirements</span></span>



| <span data-ttu-id="38ca1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="38ca1-122">Requirement</span></span> | <span data-ttu-id="38ca1-123">Value</span><span class="sxs-lookup"><span data-stu-id="38ca1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38ca1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38ca1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="38ca1-125"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38ca1-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="38ca1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38ca1-126">Library</span></span><br/> | <dl> <span data-ttu-id="38ca1-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="38ca1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38ca1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="38ca1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ca1-129">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="38ca1-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




