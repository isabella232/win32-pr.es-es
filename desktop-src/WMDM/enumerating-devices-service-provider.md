---
title: Enumerar dispositivos (WMDM)
description: Enumerar dispositivos
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Media Administrador de dispositivos, enumerar dispositivos
- Administrador de dispositivos, enumerar dispositivos
- Guía de programación, enumeración de dispositivos
- proveedores de servicios, enumerar dispositivos
- crear proveedores de servicios, enumerar dispositivos
- enumerar dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316b87f6ad3f5680e0c22da832da7b1efec24629
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103785087"
---
# <a name="enumerating-devices-wmdm"></a>Enumerar dispositivos (WMDM)

Windows Media Administrador de dispositivos mantiene una memoria caché de los dispositivos conectados que se actualizan cuando se inicia una aplicación de Windows Media Administrador de dispositivos, cuando un dispositivo Plug and Play (PnP) se conecta o desconecta, o cuando la aplicación llama a [**IWMDeviceManager2:: reinicializar**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize). Esta memoria caché se expone a la aplicación cuando llama a [**IWMDeviceManager:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) o [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2). Cada dispositivo se expone a la aplicación como una interfaz [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) . Si el proveedor de servicios está registrado para administrar dispositivos Plug and Play, Windows Media Administrador de dispositivos conocerá la lista actual de dispositivos conectados. Si el proveedor de servicios está registrado para controlar los dispositivos que no son Plug and Play, el proveedor de servicios es responsable de detectar los dispositivos conectados. Un proveedor de servicios solo se puede registrar para dispositivos PnP o no PnP, nunca ambos.

Las siguientes acciones muestran cómo Windows Media Administrador de dispositivos mantiene o actualiza su memoria caché. Tenga en cuenta que la memoria caché nunca se actualiza cuando un dispositivo que no es PnP se conecta o se desconecta.

Se inicia una aplicación de Windows Media Administrador de dispositivos

-   Windows Media Administrador de dispositivos recupera una lista de dispositivos PnP conectados del subsistema PnP y llama a [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) en el SP registrado para cada dispositivo conectado. (Detecta el proveedor de servicios correcto consultando el parámetro de dispositivo WMDMSPCLSID para el identificador de clase del proveedor de servicios responsable de este dispositivo. Consulte [parámetros del dispositivo](device-parameters.md) para obtener más información). Todos los dispositivos devueltos se agregan a la caché de dispositivos Administrador de dispositivos de Windows Media.
-   Windows Media Administrador de dispositivos encuentra todos los proveedores de servicios que no son de PnP registrados y llama a [**IMDServiceProvider:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) en cada proveedor de servicios para obtener una lista de los dispositivos de cada uno de ellos. Todos los dispositivos devueltos se agregan a la memoria caché.

La aplicación llama a IWMDeviceManager/2:: EnumDevices/2

-   Windows Media Administrador de dispositivos devuelve la lista de dispositivos almacenados en caché.

Un dispositivo PnP se conecta

-   Windows Media Administrador de dispositivos encuentra el proveedor de servicios correspondiente y llama a **IMDServiceProvider2:: CreateDevice** y agrega el dispositivo a su memoria caché.
-   Si la aplicación implementa [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media administrador de dispositivos llama a [**IWMDMNotification:: WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) con una notificación de llegada.

Un dispositivo PnP se desconecta

-   Windows Media Administrador de dispositivos quita el elemento de la memoria caché.
-   Si la aplicación implementa IWMDMNotification, Windows Media Administrador de dispositivos llama a IWMDMNotification:: WMDMMessage con una notificación de salida.

La aplicación llama a IWMDeviceManager2:: reinitialized

-   Actualiza la memoria caché con todos los dispositivos conectados.

Un dispositivo no PnP se conecta o desconecta

-   Windows Media Administrador de dispositivos no está informado de la llegada o la salida y no realiza ninguna acción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> </dl>

 

 




