---
title: Métodos IRemoteDesktopClientEvents
description: La interfaz IRemoteDesktopClientEvents expone los métodos siguientes.
ms.assetid: D8035924-736D-495D-BF78-950DAEB69774
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe59ebb3eb2fb077b53074024100c4f0861cf197
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359095"
---
# <a name="iremotedesktopclientevents-methods"></a><span data-ttu-id="bc450-103">Métodos IRemoteDesktopClientEvents</span><span class="sxs-lookup"><span data-stu-id="bc450-103">IRemoteDesktopClientEvents methods</span></span>

<span data-ttu-id="bc450-104">La interfaz [**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md) expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="bc450-104">The [**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bc450-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bc450-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="bc450-106">**Método biconnect**</span><span class="sxs-lookup"><span data-stu-id="bc450-106">**OnConnecting method**</span></span>](iremotedesktopclientevents-onconnecting.md)
</dt> <dd>

<span data-ttu-id="bc450-107">Se llama cuando el control de cliente intenta establecer una conexión a una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="bc450-107">Called when the client control attempts to establish a connection to a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-108">**Unconnected (método)**</span><span class="sxs-lookup"><span data-stu-id="bc450-108">**OnConnected method**</span></span>](iremotedesktopclientevents-onconnected.md)
</dt> <dd>

<span data-ttu-id="bc450-109">Se llama cuando el control de cliente se ha conectado a una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="bc450-109">Called when the client control has connected to a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-110">**Método OnLoginCompleted**</span><span class="sxs-lookup"><span data-stu-id="bc450-110">**OnLoginCompleted method**</span></span>](iremotedesktopclientevents-onlogincompleted.md)
</dt> <dd>

<span data-ttu-id="bc450-111">Se llama cuando el control de cliente ha iniciado sesión correctamente en una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="bc450-111">Called when the client control has successfully logged on to a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-112">**OnDisconnection (método)**</span><span class="sxs-lookup"><span data-stu-id="bc450-112">**OnDisconnected method**</span></span>](iremotedesktopclientevents-ondisconnected.md)
</dt> <dd>

<span data-ttu-id="bc450-113">Se llama cuando el control de cliente se ha desconectado de una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="bc450-113">Called when the client control has been disconnected from a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-114">**Método OnStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="bc450-114">**OnStatusChanged method**</span></span>](iremotedesktopclientevents-onstatuschanged.md)
</dt> <dd>

<span data-ttu-id="bc450-115">Se llama cuando el control de cliente ha actualizado su estado.</span><span class="sxs-lookup"><span data-stu-id="bc450-115">Called when the client control has updated its status.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-116">**Método OnAutoReconnecting**</span><span class="sxs-lookup"><span data-stu-id="bc450-116">**OnAutoReconnecting method**</span></span>](iremotedesktopclientevents-onautoreconnecting.md)
</dt> <dd>

<span data-ttu-id="bc450-117">Se llama cuando el control de cliente intenta restablecer automáticamente una conexión a una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="bc450-117">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-118">**Método OnAutoReconnected**</span><span class="sxs-lookup"><span data-stu-id="bc450-118">**OnAutoReconnected method**</span></span>](iremotedesktopclientevents-onautoreconnected.md)
</dt> <dd>

<span data-ttu-id="bc450-119">Se llama cuando el control de cliente se vuelve a conectar automáticamente a una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="bc450-119">Called when the client control has automatically reconnected to a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-120">**Método OnDialogDisplaying**</span><span class="sxs-lookup"><span data-stu-id="bc450-120">**OnDialogDisplaying method**</span></span>](iremotedesktopclientevents-ondialogdisplaying.md)
</dt> <dd>

<span data-ttu-id="bc450-121">Se llama antes de que el control muestre un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bc450-121">Called before the control displays a dialog box.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-122">**Método OnDialogDismissed**</span><span class="sxs-lookup"><span data-stu-id="bc450-122">**OnDialogDismissed method**</span></span>](iremotedesktopclientevents-ondialogdismissed.md)
</dt> <dd>

<span data-ttu-id="bc450-123">Se llama después de que se descarte un cuadro de diálogo que muestra el control de cliente.</span><span class="sxs-lookup"><span data-stu-id="bc450-123">Called after a dialog box displayed by the client control is dismissed.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-124">**Método OnNetworkStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="bc450-124">**OnNetworkStatusChanged method**</span></span>](iremotedesktopclientevents-onnetworkstatuschanged.md)
</dt> <dd>

<span data-ttu-id="bc450-125">Se llama cuando el estado de la red ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="bc450-125">Called when the network status has changed.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-126">**Método OnAdminMessageReceived**</span><span class="sxs-lookup"><span data-stu-id="bc450-126">**OnAdminMessageReceived method**</span></span>](iremotedesktopclientevents-onadminmessagereceived.md)
</dt> <dd>

<span data-ttu-id="bc450-127">Se llama cuando el control de cliente recibe un mensaje administrativo.</span><span class="sxs-lookup"><span data-stu-id="bc450-127">Called when the client control receives an administrative message.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-128">**Método OnKeyCombinationPressed**</span><span class="sxs-lookup"><span data-stu-id="bc450-128">**OnKeyCombinationPressed method**</span></span>](iremotedesktopclientevents-onkeycombinationpressed.md)
</dt> <dd>

<span data-ttu-id="bc450-129">Se le llama cuando se presionan combinaciones de teclas especiales en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="bc450-129">Called when special key combinations are pressed in the remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-130">**Método OnRemoteDesktopSizeChanged**</span><span class="sxs-lookup"><span data-stu-id="bc450-130">**OnRemoteDesktopSizeChanged method**</span></span>](iremotedesktopclientevents-onremotedesktopsizechanged.md)
</dt> <dd>

<span data-ttu-id="bc450-131">Se llama cuando el tamaño del escritorio remoto ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="bc450-131">Called when the remote desktop size has changed.</span></span>

</dd> <dt>

[<span data-ttu-id="bc450-132">**Método OnTouchPointerCursorMoved**</span><span class="sxs-lookup"><span data-stu-id="bc450-132">**OnTouchPointerCursorMoved method**</span></span>](iremotedesktopclientevents-ontouchpointercursormoved.md)
</dt> <dd>

<span data-ttu-id="bc450-133">Se llama cuando se ha cambiado el cursor del puntero táctil y la propiedad [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) está establecida en true.</span><span class="sxs-lookup"><span data-stu-id="bc450-133">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span>

</dd> </dl>

 

 