---
title: Habilitación de notificaciones
description: Habilitación de notificaciones
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Administrador de dispositivos de Windows Media, notificaciones
- Administrador de dispositivos, notificaciones
- Guía de programación, notificaciones
- aplicaciones de escritorio, notificaciones
- creación de aplicaciones de Windows Media Administrador de dispositivos, notificaciones
- Notificaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618356c9d63d20a8b6b14e6c99072074cfc75073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775234"
---
# <a name="enabling-notifications"></a><span data-ttu-id="b18a4-109">Habilitación de notificaciones</span><span class="sxs-lookup"><span data-stu-id="b18a4-109">Enabling Notifications</span></span>

<span data-ttu-id="b18a4-110">Windows Media Administrador de dispositivos declara cuatro interfaces que una aplicación puede implementar en una clase COM para recibir notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="b18a4-110">Windows Media Device Manager declares four interfaces that an application can implement in a COM class to receive event notifications.</span></span> <span data-ttu-id="b18a4-111">Estas interfaces se dividen en dos grupos, tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b18a4-111">These interfaces fall into two groups, as shown in the following table.</span></span>



| <span data-ttu-id="b18a4-112">Interfaces</span><span class="sxs-lookup"><span data-stu-id="b18a4-112">Interfaces</span></span>                                                                                                                                                | <span data-ttu-id="b18a4-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b18a4-113">Description</span></span>                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b18a4-114">**IWMDMNotification**</span><span class="sxs-lookup"><span data-stu-id="b18a4-114">**IWMDMNotification**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | <span data-ttu-id="b18a4-115">Notifica a la aplicación cuando los dispositivos o medios de almacenamiento están conectados o desconectados.</span><span class="sxs-lookup"><span data-stu-id="b18a4-115">Notifies the application when devices or storage media are connected or disconnected.</span></span>                                                                                         |
| [<span data-ttu-id="b18a4-116">**IWMDMProgress**</span><span class="sxs-lookup"><span data-stu-id="b18a4-116">**IWMDMProgress**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [<span data-ttu-id="b18a4-117">**IWMDMProgress2**</span><span class="sxs-lookup"><span data-stu-id="b18a4-117">**IWMDMProgress2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [<span data-ttu-id="b18a4-118">**IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="b18a4-118">**IWMDMProgress3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | <span data-ttu-id="b18a4-119">Un sistema de notificación muy sencillo para avisar a una aplicación sobre el progreso de cualquier evento.</span><span class="sxs-lookup"><span data-stu-id="b18a4-119">A very simple notification system to alert an application about the progress of any event.</span></span> <span data-ttu-id="b18a4-120">No es necesario que la aplicación realice ninguna acción en respuesta a estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="b18a4-120">The application is not required to take any actions in response to these messages.</span></span> |



 

<span data-ttu-id="b18a4-121">**IWMDMNotification**</span><span class="sxs-lookup"><span data-stu-id="b18a4-121">**IWMDMNotification**</span></span>

<span data-ttu-id="b18a4-122">**IWMDMNotification** alerta a la aplicación cuando plug and Play dispositivos están conectados o desconectados del equipo, así como cuando plug and Play medios de almacenamiento (como tarjetas flash) se insertan o se quitan del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b18a4-122">**IWMDMNotification** alerts the application when Plug and Play devices are connected or disconnected from the computer, as well as when Plug and Play storage media (such as flash cards) are inserted or removed from the device.</span></span> <span data-ttu-id="b18a4-123">Estas notificaciones pueden ayudar a la aplicación a actualizar su interfaz de usuario para reflejar los cambios.</span><span class="sxs-lookup"><span data-stu-id="b18a4-123">These notifications can help the application update its user interface to reflect changes.</span></span>

<span data-ttu-id="b18a4-124">Para recibir estas notificaciones, la aplicación debe registrarse para recibirlos con las interfaces de Platform SDK **IConnectionPointContainer** e **IConnectionPoint** .</span><span class="sxs-lookup"><span data-stu-id="b18a4-124">In order to receive these notifications, your application must register to receive them using the Platform SDK **IConnectionPointContainer** and **IConnectionPoint** interfaces.</span></span> <span data-ttu-id="b18a4-125">La aplicación debe registrarse para recibir eventos cuando se inicia y anular el registro cuando se cierra.</span><span class="sxs-lookup"><span data-stu-id="b18a4-125">Your application should register to receive events when it starts up, and unregister when it closes.</span></span> <span data-ttu-id="b18a4-126">Siga estos pasos para registrarse para recibir estas notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b18a4-126">Follow these steps to register to receive these notifications.</span></span>

1.  <span data-ttu-id="b18a4-127">Consulte la interfaz principal de **IWMDeviceManager** que recibió al autenticar la aplicación para **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="b18a4-127">Query the main **IWMDeviceManager** interface you received when you authenticated your application for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="b18a4-128">Llame a **IConnectionPointContainer:: FindConnectionPoint** para recuperar un punto de conexión de contenedor para las interfaces de **IWMDMNotification** .</span><span class="sxs-lookup"><span data-stu-id="b18a4-128">Call **IConnectionPointContainer::FindConnectionPoint** to retrieve a container connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="b18a4-129">Regístrese para recibir eventos mediante una llamada a **IConnectionPoint:: Advise**.</span><span class="sxs-lookup"><span data-stu-id="b18a4-129">Register to receive events by calling **IConnectionPoint::Advise**.</span></span> <span data-ttu-id="b18a4-130">Pase la clase que implementa **IWMDMNotification** y recupere una cookie, un identificador único que identifica el punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="b18a4-130">Pass in the class that implements **IWMDMNotification**, and retrieve a cookie, a unique ID that identifies your connection point.</span></span> <span data-ttu-id="b18a4-131">Debe almacenarse y usarse más adelante para anular el registro de las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="b18a4-131">This must be stored, and used later to unregister for event notifications.</span></span>

<span data-ttu-id="b18a4-132">En el código de C++ siguiente se muestra cómo puede registrarse para recibir notificaciones de **IWMDMNotification**.</span><span class="sxs-lookup"><span data-stu-id="b18a4-132">The following C++ code demonstrates how you can register to receive notifications from **IWMDMNotification**.</span></span>


```C++
HRESULT CWMDMController::RegisterForNotifications()
{
    HRESULT hr = S_OK;
    CComPtr<IConnectionPointContainer> pConxnPointCont;
    CComPtr<IConnectionPoint> pIConnPoint;

    // Get the IConnectionPointContainer interface from IWMDeviceManager.
    if (SUCCEEDED (hr = m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer, (void**) & pConxnPointCont)))
    {
        // Get a connection point from the container.
        if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
        {
            // Add ourselves as a callback handler for the connection point.
            // If we succeeded, indicate that by storing the connection point ID.
            DWORD dwCookie;
            if (SUCCEEDED (hr = pIConnPoint->Advise((IUnknown*)((IWMDMNotification*)this), &dwCookie)))
            {
                m_dwNotificationCookie = dwCookie;
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="b18a4-133">Cuando se cierre la aplicación, debe anular el registro con **IConnectionPoint** para indicar que ya no debe enviar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b18a4-133">When your application closes, you must unregister with **IConnectionPoint** to indicate that it should no longer send you notifications.</span></span> <span data-ttu-id="b18a4-134">Siga estos pasos para anular el registro de las notificaciones:</span><span class="sxs-lookup"><span data-stu-id="b18a4-134">Follow these steps to unregister for notifications:</span></span>

1.  <span data-ttu-id="b18a4-135">Consulte la interfaz principal de **IWMDeviceManager** para **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="b18a4-135">Query the main **IWMDeviceManager** interface for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="b18a4-136">Obtiene un punto de conexión para las interfaces **IWMDMNotification** .</span><span class="sxs-lookup"><span data-stu-id="b18a4-136">Get a connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="b18a4-137">Anule el registro de la aplicación para notificaciones de eventos mediante una llamada a **IConnectionPoint:: unvise**, pasando el identificador único recibido al registrarse para recibir eventos.</span><span class="sxs-lookup"><span data-stu-id="b18a4-137">Unregister your application for event notifications by calling **IConnectionPoint::Unadvise**, passing in the unique ID received when you registered to receive events.</span></span>

<span data-ttu-id="b18a4-138">El siguiente código de C++ muestra cómo anular el registro para los eventos de **IWMDMNotification** cuando se cierra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b18a4-138">The following C++ code shows how to unregister for **IWMDMNotification** events when your application closes.</span></span>


```C++
HRESULT CWMDMController::UnregisterForNotifications()
{
    HRESULT hr = S_FALSE;

    // On class initialization, we initialized the handle to -1 as a flag 
    // to indicate we had not yet registered for notifications. If registration 
    // never happened, don't bother to unregister.
    if (-1 != m_dwNotificationCookie)
    {
        CComPtr<IConnectionPointContainer> pConxnPointCont;
        CComPtr<IConnectionPoint> pIConnPoint;

        // Get the connection point container from IWMDeviceManager. 
        if (SUCCEEDED (hr = 
           m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer,
           (void**) & pConxnPointCont)))
        {
            // Get a connection point from the container.
            if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
            {
                // Remove ourselves as a callback from the connection point.
                // If successful, reset the ID to a flag value.
                if (SUCCEEDED (hr = 
                    pIConnPoint->Unadvise(m_dwNotificationCookie)))
                {
                    m_dwNotificationCookie = -1;
                    hr = S_OK;
                }
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="b18a4-139">**Usar IWMDMProgress**</span><span class="sxs-lookup"><span data-stu-id="b18a4-139">**Using IWMDMProgress**</span></span>

<span data-ttu-id="b18a4-140">Windows Media Administrador de dispositivos puede enviar los mensajes de estado de la aplicación cuando se producen acciones específicas, como la transferencia de contenido, la adquisición segura del reloj y la obtención de información de archivos DRM.</span><span class="sxs-lookup"><span data-stu-id="b18a4-140">Windows Media Device Manager can send your application status messages when specific actions, such as content transfer, secure clock acquisition, and encountering DRM file information, occur.</span></span> <span data-ttu-id="b18a4-141">La aplicación puede utilizar estos mensajes para supervisar el estado del evento o cancelar un evento.</span><span class="sxs-lookup"><span data-stu-id="b18a4-141">Your application can use these messages to monitor the status of the event or cancel an event.</span></span> <span data-ttu-id="b18a4-142">Para usar esta interfaz, implemente [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)o [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)y páselo como un parámetro a un método que aceptará un mensaje de progreso.</span><span class="sxs-lookup"><span data-stu-id="b18a4-142">To use this interface, implement [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2), or [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3), and pass it in as a parameter to a method that will accept a progress message.</span></span> <span data-ttu-id="b18a4-143">Tenga en cuenta que **IWMDMProgress3** es la interfaz superior porque proporciona un GUID de identificación que especifica la acción de la que se realiza el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="b18a4-143">Note that **IWMDMProgress3** is the superior interface because it provides an identification GUID that specifies what action is being tracked.</span></span> <span data-ttu-id="b18a4-144">Los siguientes métodos de aplicación aceptan una interfaz de progreso (los métodos de proveedor de servicios correspondientes deben poder enviar notificaciones a una interfaz enviada):</span><span class="sxs-lookup"><span data-stu-id="b18a4-144">The following application methods accept a progress interface (the corresponding service provider methods should be able to send notifications to a submitted interface):</span></span>

[<span data-ttu-id="b18a4-145">**IWMDMStorageControl::D iminar**</span><span class="sxs-lookup"><span data-stu-id="b18a4-145">**IWMDMStorageControl::Delete**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[<span data-ttu-id="b18a4-146">**IWMDMStorageControl:: Insert**</span><span class="sxs-lookup"><span data-stu-id="b18a4-146">**IWMDMStorageControl::Insert**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[<span data-ttu-id="b18a4-147">**IWMDMStorageControl:: Move**</span><span class="sxs-lookup"><span data-stu-id="b18a4-147">**IWMDMStorageControl::Move**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[<span data-ttu-id="b18a4-148">**IWMDMStorageControl:: Read**</span><span class="sxs-lookup"><span data-stu-id="b18a4-148">**IWMDMStorageControl::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[<span data-ttu-id="b18a4-149">**IWMDMStorageControl:: Rename**</span><span class="sxs-lookup"><span data-stu-id="b18a4-149">**IWMDMStorageControl::Rename**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[<span data-ttu-id="b18a4-150">**IWMDMStorageControl2::Insert2**</span><span class="sxs-lookup"><span data-stu-id="b18a4-150">**IWMDMStorageControl2::Insert2**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[<span data-ttu-id="b18a4-151">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="b18a4-151">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[<span data-ttu-id="b18a4-152">**IWMDMStorageGlobals:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="b18a4-152">**IWMDMStorageGlobals::Initialize**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[<span data-ttu-id="b18a4-153">**IWMDRMDeviceApp::AcquireDeviceData**</span><span class="sxs-lookup"><span data-stu-id="b18a4-153">**IWMDRMDeviceApp::AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)

<span data-ttu-id="b18a4-154">En la documentación de estos métodos se proporcionan ejemplos de cómo pasar una interfaz a un método.</span><span class="sxs-lookup"><span data-stu-id="b18a4-154">Examples of passing an interface into a method are given in the documentation for these methods.</span></span> <span data-ttu-id="b18a4-155">Para obtener ejemplos de cómo implementar las interfaces de devolución de llamada, vea la documentación de los métodos de **IWMDMProgress**, **IWMDMProgress2** o **IWMDMProgress3**.</span><span class="sxs-lookup"><span data-stu-id="b18a4-155">For examples of implementing the callback interfaces, see the documentation for the methods of **IWMDMProgress**, **IWMDMProgress2**, or **IWMDMProgress3**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b18a4-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b18a4-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b18a4-157">**Crear una aplicación de Windows Media Administrador de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="b18a4-157">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





