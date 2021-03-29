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
# <a name="enabling-notifications"></a>Habilitación de notificaciones

Windows Media Administrador de dispositivos declara cuatro interfaces que una aplicación puede implementar en una clase COM para recibir notificaciones de eventos. Estas interfaces se dividen en dos grupos, tal y como se muestra en la tabla siguiente.



| Interfaces                                                                                                                                                | Descripción                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | Notifica a la aplicación cuando los dispositivos o medios de almacenamiento están conectados o desconectados.                                                                                         |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | Un sistema de notificación muy sencillo para avisar a una aplicación sobre el progreso de cualquier evento. No es necesario que la aplicación realice ninguna acción en respuesta a estos mensajes. |



 

**IWMDMNotification**

**IWMDMNotification** alerta a la aplicación cuando plug and Play dispositivos están conectados o desconectados del equipo, así como cuando plug and Play medios de almacenamiento (como tarjetas flash) se insertan o se quitan del dispositivo. Estas notificaciones pueden ayudar a la aplicación a actualizar su interfaz de usuario para reflejar los cambios.

Para recibir estas notificaciones, la aplicación debe registrarse para recibirlos con las interfaces de Platform SDK **IConnectionPointContainer** e **IConnectionPoint** . La aplicación debe registrarse para recibir eventos cuando se inicia y anular el registro cuando se cierra. Siga estos pasos para registrarse para recibir estas notificaciones.

1.  Consulte la interfaz principal de **IWMDeviceManager** que recibió al autenticar la aplicación para **IConnectionPointContainer**.
2.  Llame a **IConnectionPointContainer:: FindConnectionPoint** para recuperar un punto de conexión de contenedor para las interfaces de **IWMDMNotification** .
3.  Regístrese para recibir eventos mediante una llamada a **IConnectionPoint:: Advise**. Pase la clase que implementa **IWMDMNotification** y recupere una cookie, un identificador único que identifica el punto de conexión. Debe almacenarse y usarse más adelante para anular el registro de las notificaciones de eventos.

En el código de C++ siguiente se muestra cómo puede registrarse para recibir notificaciones de **IWMDMNotification**.


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



Cuando se cierre la aplicación, debe anular el registro con **IConnectionPoint** para indicar que ya no debe enviar notificaciones. Siga estos pasos para anular el registro de las notificaciones:

1.  Consulte la interfaz principal de **IWMDeviceManager** para **IConnectionPointContainer**.
2.  Obtiene un punto de conexión para las interfaces **IWMDMNotification** .
3.  Anule el registro de la aplicación para notificaciones de eventos mediante una llamada a **IConnectionPoint:: unvise**, pasando el identificador único recibido al registrarse para recibir eventos.

El siguiente código de C++ muestra cómo anular el registro para los eventos de **IWMDMNotification** cuando se cierra la aplicación.


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



**Usar IWMDMProgress**

Windows Media Administrador de dispositivos puede enviar los mensajes de estado de la aplicación cuando se producen acciones específicas, como la transferencia de contenido, la adquisición segura del reloj y la obtención de información de archivos DRM. La aplicación puede utilizar estos mensajes para supervisar el estado del evento o cancelar un evento. Para usar esta interfaz, implemente [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)o [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)y páselo como un parámetro a un método que aceptará un mensaje de progreso. Tenga en cuenta que **IWMDMProgress3** es la interfaz superior porque proporciona un GUID de identificación que especifica la acción de la que se realiza el seguimiento. Los siguientes métodos de aplicación aceptan una interfaz de progreso (los métodos de proveedor de servicios correspondientes deben poder enviar notificaciones a una interfaz enviada):

[**IWMDMStorageControl::D iminar**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[**IWMDMStorageControl:: Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[**IWMDMStorageControl:: Move**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[**IWMDMStorageControl:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[**IWMDMStorageControl:: Rename**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[**IWMDMStorageGlobals:: Initialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)

En la documentación de estos métodos se proporcionan ejemplos de cómo pasar una interfaz a un método. Para obtener ejemplos de cómo implementar las interfaces de devolución de llamada, vea la documentación de los métodos de **IWMDMProgress**, **IWMDMProgress2** o **IWMDMProgress3**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear una aplicación de Windows Media Administrador de dispositivos**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





