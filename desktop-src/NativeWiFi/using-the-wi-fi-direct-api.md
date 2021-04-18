---
description: Muestra cómo usar Wi-Fi funciones directas en aplicaciones de escritorio.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Usar las funciones directas Wi-Fi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8850f5b278a158e32f78118cf5d0d408c123192e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667134"
---
# <a name="using-the-wi-fi-direct-functions"></a>Usar las funciones directas Wi-Fi

En este tema se muestra cómo usar Wi-Fi funciones directas en aplicaciones de escritorio. A partir de Windows 8 y Windows Server 2012, Wi-Fi funciones directas se agregaron a la API WiFi nativa.

La característica Wi-Fi Direct se basa en el desarrollo de la Wi-Fi especificación técnica punto a punto v 1.1 de la Alianza de Wi-Fi (consulte las [especificaciones publicadas de Wi-Fi Alliance](https://www.wi-fi.org/)). El objetivo del Wi-Fi especificación técnica punto a punto es proporcionar una solución para Wi-Fi la conectividad de dispositivo a dispositivo sin necesidad de que un punto de acceso inalámbrico (AP inalámbrico) Configure la conexión o el uso del mecanismo Wi-Fi ad hoc (IBSS) existente.

> [!Note]  
> El modo ad hoc podría no estar disponible en versiones futuras de Windows. A partir de Windows 8.1 y Windows Server 2012 R2, utilice Wi-Fi Direct en su lugar.

 

Las funciones siguientes admiten la característica Wi-Fi Direct.

-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) : indica que la aplicación desea cancelar una función de [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) pendiente que no se ha completado.
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) : cierra un identificador para el servicio Wi-Fi Direct.
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) : cierra una sesión después de una llamada correcta previamente a la función [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) : abre un identificador para el servicio Wi-Fi Direct y negocia una versión de la API de Wi-Fi Direct que se va a usar.
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) : recupera y aplica un perfil almacenado para un Wi-Fi dispositivo heredado directo.
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) : inicia una conexión a petición a un dispositivo Wi-Fi Direct específico, que se ha emparejado previamente a través de la experiencia de emparejamiento de Windows.
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) : actualiza la visibilidad del dispositivo para la dirección de dispositivo Wi-Fi Direct para un nodo de dispositivo directo de Wi-Fi directo instalado.
-   [**WFD \_ \_Devolución de \_ \_ llamada completa de la sesión abierta**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : define la función de devolución de llamada a la que llama la función [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) cuando se completa la operación **WFDStartOpenSession**

En el caso de una aplicación de escritorio, la característica Wi-Fi Direct requiere que los dispositivos Wi-FI Direct estén emparejados previamente por el usuario con la interfaz de usuario de la experiencia de emparejamiento de Windows. Una vez completado este emparejamiento, se almacena un perfil que permite usar las funciones de Wi-Fi directo para iniciar una sesión Wi-Fi Direct para establecer una conexión entre el Wi-Fi dispositivos directos.

Para usar Wi-Fi Direct, una aplicación primero debe obtener un identificador para el servicio Wi-Fi Direct llamando a la función [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) . El identificador Wi-Fi directo (WFD) devuelto por la función **WFDOpenHandle** se utiliza para las llamadas a funciones Wi-Fi directas posteriores realizadas a la Wi-Fi servicio directo.

La función [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) inicia una operación asincrónica para iniciar una conexión a petición a un dispositivo Wi-Fi Direct específico. El dispositivo Wi-Fi de destino debe haberse emparejado anteriormente a través de la experiencia de emparejamiento de Windows. Cuando se completa la operación asincrónica, se llama a la función de devolución de llamada especificada en el parámetro *pfnCallback* .

Una vez que se realiza una aplicación mediante el servicio de Wi-Fi Direct, la aplicación debe llamar a la función [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) para indicar al Wi-Fi servicio directo que la aplicación se realiza mediante el servicio. Esto permite al Wi-Fi servicio directo liberar los recursos utilizados por la aplicación.

Para obtener más información sobre Wi-Fi directo para su uso en aplicaciones de la tienda Windows, consulte [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) y las clases relacionadas en el espacio de nombres [**Windows. networking. Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Otros recursos**
</dt> <dt>

[Acerca de WiFi nativo](about-native-wifi.md)
</dt> <dt>

[Acerca de la API nativa WiFi](about-the-native-wifi-api.md)
</dt> <dt>

[Acerca de la característica Wi-Fi Direct](about-the-wi-fi-direct-api.md)
</dt> <dt>

**Referencia**
</dt> <dt>

[**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[**\_devolución de \_ \_ llamada completa de sesión abierta de WFD \_**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
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

 

 
