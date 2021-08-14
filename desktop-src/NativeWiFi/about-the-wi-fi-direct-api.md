---
description: Native Wifi API contiene un conjunto de funciones que admiten el uso de Wi-Fi Direct para aplicaciones de escritorio.
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: Acerca de la característica Wi-Fi Direct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2816938b3e2d9156f2a97b67990386af2d5d780aa0226316cccc5edd0f2a4b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620220"
---
# <a name="about-the-wi-fi-direct-feature"></a>Acerca de la característica Wi-Fi Direct

Native Wifi API contiene un conjunto de funciones que admiten el uso de Wi-Fi Direct para aplicaciones de escritorio. A partir de Windows 8 y Windows Server 2012, Wi-Fi funciones de Direct se agregaron a native Wifi API.

La característica Wi-Fi Direct se basa en el desarrollo de la especificación técnica punto a punto de Wi-Fi v1.1 por parte de Wi-Fi Alliance (consulte Especificaciones publicadas de [Wi-Fi Alliance).](https://www.wi-fi.org/) El objetivo de la especificación técnica punto a punto de Wi-Fi es proporcionar una solución para la conectividad de dispositivo a dispositivo Wi-Fi sin necesidad de un punto de acceso inalámbrico (AP inalámbrico) para configurar la conexión o el uso del mecanismo ad hoc (IBSS) de Wi-Fi existente.

> [!Note]  
> Es posible que el modo ad hoc no esté disponible en versiones futuras de Windows. A partir de Windows 8.1 y Windows Server 2012 R2, use Wi-Fi Direct en su lugar.

 

Para una aplicación de escritorio, la característica Wi-Fi Direct requiere que el usuario empareje previamente los dispositivos Wi-FI Direct con la interfaz de usuario de la experiencia de emparejamiento de Windows. Una vez completado este emparejamiento, se almacena un perfil que permite usar las funciones de Wi-Fi Direct para iniciar una sesión de Wi-Fi Direct con el fin de establecer una conexión entre los dispositivos Wi-Fi Direct.

Las siguientes funciones admiten la característica Wi-Fi Direct.

-   [**WFDCancelOpenSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) indica que la aplicación quiere cancelar una función [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) pendiente que no se ha completado.
-   [**WFDCloseHandle:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) cierra un identificador al servicio Wi-Fi Direct.
-   [**WFDCloseSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) cierra una sesión después de una llamada previamente correcta a la [**función WFDStartOpenSession.**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDOpenHandle:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) abre un identificador para el servicio Wi-Fi Direct y negocia una versión de direct API de Wi-FI que se usará.
-   [**WFDOpenLegacySession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) recupera y aplica un perfil almacenado para un Wi-Fi heredado directo.
-   [**WFDStartOpenSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) inicia una conexión a petición a un dispositivo Wi-Fi Direct específico, que se ha emparejado previamente a través de la experiencia Windows emparejamiento.
-   [**WFDUpdateDeviceVisibility:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) actualiza la visibilidad del dispositivo para la Wi-Fi de dispositivo direct para un nodo de dispositivo Wi-Fi direct determinado.
-   [**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ CALLBACK:**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) define la función de devolución de llamada a la que llama la función [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) cuando se completa la operación **WFDStartOpenSession.**

Para más información sobre el uso de Wi-Fi Direct en una aplicación de escritorio, consulte Uso de [las Wi-Fi direct.](using-the-wi-fi-direct-api.md)

Para obtener más información sobre Wi-Fi Direct para su uso en aplicaciones de Windows Store, vea [**PeerConexión**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) y clases relacionadas en [**el Windows. Espacio de nombres Networking.Proximity.**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Otros recursos**
</dt> <dt>

[Acerca de Wi-Fi nativo](about-native-wifi.md)
</dt> <dt>

[Acerca de la API Wi-Fi nativa](about-the-native-wifi-api.md)
</dt> <dt>

[Acerca de la API ad hoc inalámbrica](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Uso de las Wi-Fi Direct](using-the-wi-fi-direct-api.md)
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

 

 
