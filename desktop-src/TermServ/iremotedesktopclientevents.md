---
title: Interfaz IRemoteDesktopClientEvents
description: Proporciona métodos que reciben información del servidor relacionada con los eventos de control de cliente.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IRemoteDesktopClientEvents
- Servicios de Escritorio remoto de la interfaz IRemoteDesktopClientEvents, descrito
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079375"
---
# <a name="iremotedesktopclientevents-interface"></a><span data-ttu-id="017e5-105">Interfaz IRemoteDesktopClientEvents</span><span class="sxs-lookup"><span data-stu-id="017e5-105">IRemoteDesktopClientEvents interface</span></span>

<span data-ttu-id="017e5-106">Proporciona métodos que reciben información del servidor relacionada con los eventos de control de cliente.</span><span class="sxs-lookup"><span data-stu-id="017e5-106">Provides methods that receive information from the server that are related to client control events.</span></span> <span data-ttu-id="017e5-107">Los eventos incluyen la conexión y desconexión, las solicitudes del modo de pantalla completa, el inicio de sesión correcto y las condiciones de error.</span><span class="sxs-lookup"><span data-stu-id="017e5-107">Events include connecting and disconnecting, full-screen mode requests, successful logon, and error conditions.</span></span>

## <a name="members"></a><span data-ttu-id="017e5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="017e5-108">Members</span></span>

<span data-ttu-id="017e5-109">La interfaz **IRemoteDesktopClientEvents** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="017e5-109">The **IRemoteDesktopClientEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="017e5-110">**IRemoteDesktopClientEvents** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="017e5-110">**IRemoteDesktopClientEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="017e5-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="017e5-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="017e5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="017e5-112">Methods</span></span>

<span data-ttu-id="017e5-113">La interfaz **IRemoteDesktopClientEvents** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="017e5-113">The **IRemoteDesktopClientEvents** interface has these methods.</span></span>



| <span data-ttu-id="017e5-114">Método</span><span class="sxs-lookup"><span data-stu-id="017e5-114">Method</span></span>                                                                                      | <span data-ttu-id="017e5-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="017e5-115">Description</span></span>                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="017e5-116">**OnAdminMessageReceived**</span><span class="sxs-lookup"><span data-stu-id="017e5-116">**OnAdminMessageReceived**</span></span>](iremotedesktopclientevents-onadminmessagereceived.md)         | <span data-ttu-id="017e5-117">Se llama cuando el control de cliente recibe un mensaje administrativo.</span><span class="sxs-lookup"><span data-stu-id="017e5-117">Called when the client control receives an administrative message.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="017e5-118">**OnAutoReconnected**</span><span class="sxs-lookup"><span data-stu-id="017e5-118">**OnAutoReconnected**</span></span>](iremotedesktopclientevents-onautoreconnected.md)                   | <span data-ttu-id="017e5-119">Se llama cuando el control de cliente se vuelve a conectar automáticamente a una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="017e5-119">Called when the client control has automatically reconnected to a remote session.</span></span> <br/>                                                                       |
| [<span data-ttu-id="017e5-120">**OnAutoReconnecting**</span><span class="sxs-lookup"><span data-stu-id="017e5-120">**OnAutoReconnecting**</span></span>](iremotedesktopclientevents-onautoreconnecting.md)                 | <span data-ttu-id="017e5-121">Se llama cuando el control de cliente intenta restablecer automáticamente una conexión a una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="017e5-121">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span> <br/>                                                  |
| [<span data-ttu-id="017e5-122">**Conectado**</span><span class="sxs-lookup"><span data-stu-id="017e5-122">**OnConnected**</span></span>](iremotedesktopclientevents-onconnected.md)                               | <span data-ttu-id="017e5-123">Se llama cuando el control de cliente se ha conectado a una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="017e5-123">Called when the client control has connected to a remote session.</span></span><br/>                                                                                        |
| [<span data-ttu-id="017e5-124">**Conectar**</span><span class="sxs-lookup"><span data-stu-id="017e5-124">**OnConnecting**</span></span>](iremotedesktopclientevents-onconnecting.md)                             | <span data-ttu-id="017e5-125">Se llama cuando el control de cliente intenta establecer una conexión a una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="017e5-125">Called when the client control attempts to establish a connection to a remote session.</span></span> <br/>                                                                  |
| [<span data-ttu-id="017e5-126">**OnDialogDismissed**</span><span class="sxs-lookup"><span data-stu-id="017e5-126">**OnDialogDismissed**</span></span>](iremotedesktopclientevents-ondialogdismissed.md)                   | <span data-ttu-id="017e5-127">Se llama después de que se descarte un cuadro de diálogo que muestra el control de cliente.</span><span class="sxs-lookup"><span data-stu-id="017e5-127">Called after a dialog box displayed by the client control is dismissed.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="017e5-128">**OnDialogDisplaying**</span><span class="sxs-lookup"><span data-stu-id="017e5-128">**OnDialogDisplaying**</span></span>](iremotedesktopclientevents-ondialogdisplaying.md)                 | <span data-ttu-id="017e5-129">Se llama antes de que el control muestre un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="017e5-129">Called before the control displays a dialog box.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="017e5-130">**OnDisconnection**</span><span class="sxs-lookup"><span data-stu-id="017e5-130">**OnDisconnected**</span></span>](iremotedesktopclientevents-ondisconnected.md)                         | <span data-ttu-id="017e5-131">Se llama cuando el control de cliente se ha desconectado de una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="017e5-131">Called when the client control has been disconnected from a remote session.</span></span> <br/>                                                                             |
| [<span data-ttu-id="017e5-132">**OnKeyCombinationPressed**</span><span class="sxs-lookup"><span data-stu-id="017e5-132">**OnKeyCombinationPressed**</span></span>](iremotedesktopclientevents-onkeycombinationpressed.md)       | <span data-ttu-id="017e5-133">Se le llama cuando se presionan combinaciones de teclas especiales en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="017e5-133">Called when special key combinations are pressed in the remote session.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="017e5-134">**OnLoginCompleted**</span><span class="sxs-lookup"><span data-stu-id="017e5-134">**OnLoginCompleted**</span></span>](iremotedesktopclientevents-onlogincompleted.md)                     | <span data-ttu-id="017e5-135">Se llama cuando el control de cliente ha iniciado sesión correctamente en una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="017e5-135">Called when the client control has successfully logged on to a remote session.</span></span> <br/>                                                                          |
| [<span data-ttu-id="017e5-136">**OnNetworkStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="017e5-136">**OnNetworkStatusChanged**</span></span>](iremotedesktopclientevents-onnetworkstatuschanged.md)         | <span data-ttu-id="017e5-137">Se llama cuando el estado de la red ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="017e5-137">Called when the network status has changed.</span></span> <br/>                                                                                                             |
| [<span data-ttu-id="017e5-138">**OnRemoteDesktopSizeChanged**</span><span class="sxs-lookup"><span data-stu-id="017e5-138">**OnRemoteDesktopSizeChanged**</span></span>](iremotedesktopclientevents-onremotedesktopsizechanged.md) | <span data-ttu-id="017e5-139">Se llama cuando el tamaño del escritorio remoto ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="017e5-139">Called when the remote desktop size has changed.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="017e5-140">**OnStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="017e5-140">**OnStatusChanged**</span></span>](iremotedesktopclientevents-onstatuschanged.md)                       | <span data-ttu-id="017e5-141">Se llama cuando el control de cliente ha actualizado su estado.</span><span class="sxs-lookup"><span data-stu-id="017e5-141">Called when the client control has updated its status.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="017e5-142">**OnTouchPointerCursorMoved**</span><span class="sxs-lookup"><span data-stu-id="017e5-142">**OnTouchPointerCursorMoved**</span></span>](iremotedesktopclientevents-ontouchpointercursormoved.md)   | <span data-ttu-id="017e5-143">Se llama cuando se ha cambiado el cursor del puntero táctil y la propiedad [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) está establecida en true.</span><span class="sxs-lookup"><span data-stu-id="017e5-143">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="017e5-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="017e5-144">Requirements</span></span>



| <span data-ttu-id="017e5-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="017e5-145">Requirement</span></span> | <span data-ttu-id="017e5-146">Value</span><span class="sxs-lookup"><span data-stu-id="017e5-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="017e5-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="017e5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="017e5-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="017e5-148">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="017e5-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="017e5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="017e5-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="017e5-150">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="017e5-151">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="017e5-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="017e5-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="017e5-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="017e5-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="017e5-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="017e5-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="017e5-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="017e5-155">CLSID</span><span class="sxs-lookup"><span data-stu-id="017e5-155">CLSID</span></span><br/>                    | <span data-ttu-id="017e5-156">CLSID \_ RemoteDesktopClient se define como EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span><span class="sxs-lookup"><span data-stu-id="017e5-156">CLSID\_RemoteDesktopClient is defined as EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span></span><br/>       |
| <span data-ttu-id="017e5-157">IID</span><span class="sxs-lookup"><span data-stu-id="017e5-157">IID</span></span><br/>                      | <span data-ttu-id="017e5-158">DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="017e5-158">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="017e5-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="017e5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="017e5-160">Referencia de controles ActiveX Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="017e5-160">Remote Desktop ActiveX control reference</span></span>](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

