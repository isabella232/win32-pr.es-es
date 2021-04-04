---
title: Sustitución de protocolo
description: Sustitución de protocolo
ms.assetid: 61db5e2b-4858-446e-9a27-e0305b46683d
keywords:
- SDK de Windows Media Format, sustitución de protocolo
- Advanced Systems Format (ASF), sustitución de protocolo
- ASF (formato de sistemas avanzados), sustitución de protocolo
- sustitución de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2de8d0496467535f5740a10082f82e285c11ef6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077320"
---
# <a name="protocol-rollover"></a>Sustitución de protocolo

La sustitución de protocolos es un proceso por el que el objeto lector detecta el mejor protocolo de streaming disponible en un servidor. El lector utiliza la sustitución de protocolo cada vez que abre una dirección URL que contiene un esquema "MMS".

El lector admite varios protocolos:

-   Protocolo de streaming en tiempo real (RTSP)
-   Protocolo de transferencia de hipertexto (HTTP)
-   Microsoft Media Server (MMS)

Los protocolos RTSP y MMS tienen dos versiones: una con [*UDP*](wmformat-glossary.md) como el protocolo de entrega subyacente y la otra mediante TCP.

El objeto lector siempre usa TCP para los comandos de control de reproducción, pero puede usar TCP o UDP para la entrega del contenido transmitido por secuencias. UDP es preferible para la entrega de contenido, porque impone menos sobrecarga de ancho de banda que TCP. El protocolo TCP garantiza un transporte confiable a través del uso de "circuitos virtuales", pero el costo de hacerlo significa que TCP no es tan adecuado para flujos multimedia digitales, donde el uso eficaz del ancho de banda es más importante que los paquetes perdidos ocasionales.

Cuando una dirección URL especifica "mms://", el lector intenta usar los siguientes protocolos para la entrega de datos, en el siguiente orden:

1.  RTSPU (RTSP con UDP)
2.  RTSPt (RTSP con TCP)
3.  MMSU (MMS mediante UDP)
4.  MMST (MMS con TCP)
5.  HTTP

HTTP es un protocolo unidireccional basado en TCP y es el protocolo que usan los servidores Web. El streaming con HTTP es menos eficaz que el uso de RTSP. Sin embargo, la mayoría de los firewalls están configurados para aceptar solicitudes HTTP, mientras que normalmente rechazan otros protocolos de streaming.

Windows Media Services 9 series en Microsoft Windows Server 2003 rechazará todas las solicitudes de MMSU o MMST de un lector del SDK de Windows Media Format, ya que RTSP es el protocolo de streaming preferido. Windows Media Services versión 4,1 y versiones anteriores no son compatibles con RTSP. En este caso, el objeto de lector recurre a MMSU o HTTP.

La sustitución de protocolos no se aplica si el esquema de direcciones URL proporciona un protocolo específico, como "rtspu://" para RTSPU o "https://" para HTTP. Si el esquema de la dirección URL es "rtsp://", el lector intenta RTSPU y RTSPt, pero no otros.

Después de que el lector abra un archivo, puede consultar el protocolo que está usando llamando al método [**IWMReaderAdvanced2:: GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname) en el lector. Mientras el contenido se transmite o se descarga, este método devuelve el nombre en cuanto el contenido se almacena por completo en la memoria caché, el método **GetProtocolName** devuelve la cadena "cache".

Para obtener los nombres de todos los protocolos de Windows Media Server que admite el lector, llame al método [**IWMReaderNetworkConfig:: GetSupportedProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getsupportedprotocolname) en el lector. Puede deshabilitar uno o varios de los protocolos en la lista de sustitución de protocolos del lector mediante la interfaz **IWMReaderNetworkConfig** . Por ejemplo, el método [**IWMReaderNetworkConfig:: SetEnableTCP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenabletcp) habilita o deshabilita los protocolos basados en TCP y [**IWMReaderNetworkConfig:: SetEnableUDP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp) habilita o deshabilita los protocolos basados en UDP. Estos métodos solo se aplican a la sustitución de protocolo; los protocolos siguen estando disponibles si el esquema de direcciones URL contiene un protocolo específico. Normalmente no hay ningún motivo para deshabilitar cualquiera de los protocolos que se usan en la sustitución del protocolo. Si lo hace, puede degradar el rendimiento. Sin embargo, puede ser útil para realizar pruebas.

 

 




