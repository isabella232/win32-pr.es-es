---
description: El \_ método get Owner recupera el propietario de la ventana actual.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: Método CBaseControlWindow.get_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8f8e3d4a331dbc66397a7b0058fcefcede2cdbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670888"
---
# <a name="cbasecontrolwindowget_owner-method"></a><span data-ttu-id="6b962-103">CBaseControlWindow. Get \_ Owner (método)</span><span class="sxs-lookup"><span data-stu-id="6b962-103">CBaseControlWindow.get\_Owner method</span></span>

<span data-ttu-id="6b962-104">El `get_Owner` método recupera el propietario de la ventana actual.</span><span class="sxs-lookup"><span data-stu-id="6b962-104">The `get_Owner` method retrieves the current window owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b962-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b962-105">Syntax</span></span>


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a><span data-ttu-id="6b962-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b962-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b962-107">*Propietario*</span><span class="sxs-lookup"><span data-stu-id="6b962-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="6b962-108">Puntero al propietario de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6b962-108">Pointer to the window owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b962-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b962-109">Return value</span></span>

<span data-ttu-id="6b962-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6b962-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b962-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b962-111">Remarks</span></span>

<span data-ttu-id="6b962-112">La ventana de vídeo puede reproducirse en un entorno de documento.</span><span class="sxs-lookup"><span data-stu-id="6b962-112">The video window can play back within a document environment.</span></span> <span data-ttu-id="6b962-113">Para ello, se debe hacer que la ventana sea un elemento secundario de otra ventana (para que se recorte y se mueva correctamente).</span><span class="sxs-lookup"><span data-stu-id="6b962-113">To do this, the window must be made a child of another window (so that it is clipped and moved appropriately).</span></span> <span data-ttu-id="6b962-114">Esta propiedad permite establecer y recuperar el propietario de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6b962-114">This property allows the owner of the window to be set and retrieved.</span></span> <span data-ttu-id="6b962-115">Cuando la ventana es propiedad de otra ventana, simplemente llama a la función **SetParent** de Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="6b962-115">When the window is owned by another window, it simply calls the Microsoft Win32 **SetParent** function.</span></span> <span data-ttu-id="6b962-116">Una aplicación que llama a esta función cambiará los estilos de ventana para establecer el \_ bit de WS secundario en.</span><span class="sxs-lookup"><span data-stu-id="6b962-116">An application calling this function will change the window styles to set the WS\_CHILD bit on.</span></span>

<span data-ttu-id="6b962-117">Cuando la ventana es propiedad de otra ventana, reenvía automáticamente determinados conjuntos de mensajes (en particular, los mensajes del mouse y del teclado).</span><span class="sxs-lookup"><span data-stu-id="6b962-117">When the window is owned by another window, it will automatically forward certain sets of messages (in particular, mouse and keyboard messages).</span></span> <span data-ttu-id="6b962-118">Esto permite que una aplicación realice una edición sencilla de la zona activa y otras interacciones.</span><span class="sxs-lookup"><span data-stu-id="6b962-118">This allows an application to do simple hot-spot editing and other interactions.</span></span>

<span data-ttu-id="6b962-119">Esta función miembro está pensada para que la llamen los objetos externos a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y, por tanto, bloquea la sección crítica para sincronizar con el filtro asociado.</span><span class="sxs-lookup"><span data-stu-id="6b962-119">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="6b962-120">Llame a la función miembro [**CBaseControlWindow:: GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) para recuperar esta propiedad si no llama a desde un objeto externo.</span><span class="sxs-lookup"><span data-stu-id="6b962-120">Call the [**CBaseControlWindow::GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b962-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b962-121">Requirements</span></span>



| <span data-ttu-id="6b962-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b962-122">Requirement</span></span> | <span data-ttu-id="6b962-123">Value</span><span class="sxs-lookup"><span data-stu-id="6b962-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b962-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b962-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6b962-125"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b962-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6b962-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6b962-126">Library</span></span><br/> | <dl> <span data-ttu-id="6b962-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6b962-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b962-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b962-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b962-129">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="6b962-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




