---
description: Muestra cómo usar funciones Wi-Fi Direct en aplicaciones de escritorio.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Uso de las Wi-Fi Direct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8850f5b278a158e32f78118cf5d0d408c123192e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069427"
---
# <a name="using-the-wi-fi-direct-functions"></a>Uso de las Wi-Fi Direct

En estos temas se muestra cómo usar Wi-Fi direct en aplicaciones de escritorio. A partir de Windows 8 y Windows Server 2012, Wi-Fi funciones directas se agregaron a la API Wi-Fi nativa.

La característica Wi-Fi Direct se basa en el desarrollo de la especificación técnica punto a punto de Wi-Fi v1.1 por parte de Wi-Fi Alliance (consulte Especificaciones publicadas de [Wi-Fi Alliance).](https://www.wi-fi.org/) El objetivo de la especificación técnica punto a punto de Wi-Fi es proporcionar una solución para la conectividad de dispositivo Wi-Fi dispositivo sin necesidad de un punto de acceso inalámbrico (AP inalámbrico) para configurar la conexión o el uso del mecanismo ad hoc (IBSS) de Wi-Fi existente.

> [!Note]  
> Es posible que el modo ad hoc no esté disponible en versiones futuras de Windows. A partir de Windows 8.1 y Windows Server 2012 R2, use Wi-Fi Direct en su lugar.

 

Las siguientes funciones admiten la característica Wi-Fi Direct.

-   [**WFDCancelOpenSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) indica que la aplicación quiere cancelar una función [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) pendiente que no se ha completado.
-   [**WFDCloseHandle:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) cierra un identificador al servicio Wi-Fi Direct.
-   [**WFDCloseSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) cierra una sesión después de una llamada previamente correcta a la [**función WFDStartOpenSession.**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDOpenHandle:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) abre un identificador para el servicio Wi-Fi Direct y negocia una versión de direct API de Wi-FI que se usará.
-   [**WFDOpenLegacySession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) recupera y aplica un perfil almacenado para un Wi-Fi de direct heredado.
-   [**WFDStartOpenSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) inicia una conexión a petición a un dispositivo Wi-Fi Direct específico, que se ha emparejado previamente a través de la experiencia Windows emparejamiento.
-   [**WFDUpdateDeviceVisibility:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) actualiza la visibilidad del dispositivo para Wi-Fi dirección del dispositivo direct para un nodo de dispositivo Wi-Fi direct determinado.
-   [**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ CALLBACK:**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) define la función de devolución de llamada a la que llama la función [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) cuando se completa la operación **WFDStartOpenSession.**

Para una aplicación de escritorio, la característica Wi-Fi Direct requiere que el usuario empareja previamente los dispositivos Wi-FI Direct con la interfaz de usuario de la experiencia de emparejamiento de Windows. Una vez completado este emparejamiento, se almacena un perfil que permite usar las funciones de Wi-Fi Direct para iniciar una sesión de Wi-Fi Direct con el fin de establecer una conexión entre los dispositivos Wi-Fi Direct.

Para usar Wi-Fi Direct, una aplicación debe obtener primero un identificador para el servicio Wi-Fi Direct mediante una llamada a la [**función WFDOpenHandle.**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) El Wi-Fi direct (WFD) devuelto por la función **WFDOpenHandle** se usa para las posteriores llamadas de función Wi-Fi Direct realizadas al servicio Wi-Fi Direct.

La [**función WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) inicia una operación asincrónica para iniciar una conexión a petición a un dispositivo Wi-Fi Direct. El dispositivo Wi-Fi destino se debe haber emparejado previamente a través de la Windows emparejamiento. Cuando se completa la operación asincrónica, se llama a la función de devolución de llamada especificada en el *parámetro pfnCallback.*

Una vez que se realiza una aplicación mediante el servicio Wi-Fi Direct, la aplicación debe llamar a la función [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) para indicar al servicio Wi-Fi Direct que la aplicación se realiza mediante el servicio . Esto permite que el Wi-Fi Direct libere los recursos usados por la aplicación.

Para obtener más información sobre Wi-Fi Direct para su uso en Windows Store, vea [**PeerConexión**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) y clases relacionadas en [**el Windows. Espacio de nombres Networking.Proximity.**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Otros recursos**
</dt> <dt>

[Acerca de Wi-Fi nativo](about-native-wifi.md)
</dt> <dt>

[Acerca de la API Wi-Fi nativa](about-the-native-wifi-api.md)
</dt> <dt>

[Acerca de la característica Wi-Fi Direct](about-the-wi-fi-direct-api.md)
</dt> <dt>

**Referencia**
</dt> <dt>

[**PeerConexión**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[**DEVOLUCIÓN DE \_ LLAMADA COMPLETA DE SESIÓN ABIERTA \_ \_ \_ DE WFD**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
