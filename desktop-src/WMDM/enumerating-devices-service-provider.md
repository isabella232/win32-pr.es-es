---
title: Enumeración de dispositivos (WMDM)
description: Windows Los Administrador de dispositivos mantienen una memoria caché de dispositivos conectados. Obtenga información sobre Windows media Administrador de dispositivos mantiene o actualiza su memoria caché.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Elementos Administrador de dispositivos, enumeración de dispositivos
- Administrador de dispositivos, enumerar dispositivos
- guía de programación, enumeración de dispositivos
- proveedores de servicios, enumerar dispositivos
- crear proveedores de servicios, enumerar dispositivos
- enumerar dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500375f01e718ab6f9824868ffabd7c83e11c3e812ce0288f0c15186bc1d2de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767055"
---
# <a name="enumerating-devices-wmdm"></a>Enumeración de dispositivos (WMDM)

Windows Media Administrador de dispositivos mantiene una memoria caché de dispositivos conectados que se actualiza cuando se inicia una aplicación de Windows Media Administrador de dispositivos, cuando un dispositivo Plug and Play (PnP) se conecta o se desconecta, o cuando la aplicación llama a [**IWMDeviceManager2::Reinicializar**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize). Esta memoria caché se expone a la aplicación cuando llama a [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) o [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2). Cada dispositivo se expone a la aplicación como una [**interfaz IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) Si el proveedor de servicios está registrado para controlar dispositivos PnP, Windows Media Administrador de dispositivos conocerá la lista actual de dispositivos conectados. Si el proveedor de servicios está registrado para controlar dispositivos que no son PnP, el proveedor de servicios es responsable de detectar los dispositivos conectados. Un proveedor de servicios solo se puede registrar para dispositivos PnP o no PnP, nunca ambos.

Las siguientes acciones muestran cómo Windows media Administrador de dispositivos mantiene o actualiza su memoria caché. Tenga en cuenta que la memoria caché nunca se actualiza cuando un dispositivo que no es PnP se conecta o se desconecta.

Se inicia Windows aplicación Administrador de dispositivos multimedia

-   Windows Media Administrador de dispositivos recupera una lista de dispositivos PnP conectados del subsistema PnP y llama a [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) en el SP registrado para cada dispositivo conectado. (Detecta el proveedor de servicios correcto consultando el parámetro de dispositivo WMDMSPCLSID para el identificador de clase del proveedor de servicios responsable de este dispositivo. Consulte [Parámetros del dispositivo](device-parameters.md) para obtener más información). Todos los dispositivos devueltos se agregan a la Windows multimedia Administrador de dispositivos caché de dispositivos.
-   Windows Media Administrador de dispositivos encuentra todos los proveedores de servicios que no son PnP registrados con él y llama a [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) en cada proveedor de servicios para obtener una lista de dispositivos de cada uno. Todos los dispositivos devueltos se agregan a la memoria caché.

La aplicación llama a IWMDeviceManager/2::EnumDevices/2

-   Windows Media Administrador de dispositivos devuelve su lista de dispositivos almacenados en caché.

Se conecta un dispositivo PnP

-   Windows El Administrador de dispositivos busca el proveedor de servicios pertinente y llama a **IMDServiceProvider2::CreateDevice** y agrega el dispositivo a su memoria caché.
-   Si la aplicación implementa [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Administrador de dispositivos llama a [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) con una notificación de llegada.

Un dispositivo PnP se desconecta

-   Windows El Administrador de dispositivos quita el elemento de su memoria caché.
-   Si la aplicación implementa IWMDMNotification, Windows Media Administrador de dispositivos llama a IWMDMNotification::WMDMMessage con una notificación de salida.

La aplicación llama a IWMDeviceManager2::Reinitialize

-   Actualiza la memoria caché con todos los dispositivos conectados.

Un dispositivo que no es PnP se conecta o se desconecta

-   Windows Los Administrador de dispositivos no se informan de la llegada o salida y no realiza ninguna acción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> </dl>

 

 




