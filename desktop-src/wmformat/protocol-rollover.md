---
title: Suversión de protocolo
description: Suversión de protocolo
ms.assetid: 61db5e2b-4858-446e-9a27-e0305b46683d
keywords:
- Windows SDK de formato multimedia, suversión de protocolo
- Formato de sistemas avanzados (ASF), suversión de protocolo
- ASF (formato de sistemas avanzados), suversión de protocolo
- suversión de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ea5ae997bfcc93ed07972575b02fb58d821e902f57268c6dc274b1d11d95c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846133"
---
# <a name="protocol-rollover"></a>Suversión de protocolo

La suversión de protocolos es un proceso por el que el objeto lector detecta el mejor protocolo de streaming disponible desde un servidor. El lector usa la suversión de protocolo cada vez que abre una dirección URL que contiene un esquema "mms".

El lector admite varios protocolos:

-   Protocolo de streaming en tiempo real (RTSP)
-   Protocolo de transferencia de hipertexto (HTTP)
-   Microsoft Media Server (MMS)

Los protocolos RTSP y MMS vienen en dos tipos, uno con [*UDP*](wmformat-glossary.md) como protocolo de entrega subyacente y el otro con TCP.

El objeto lector siempre usa TCP para los comandos de control de reproducción, pero puede usar TCP o UDP para la entrega del contenido transmitido. UDP es preferible para la entrega de contenido, ya que impone menos sobrecarga de ancho de banda que TCP. El protocolo TCP garantiza un transporte confiable mediante el uso de "circuitos virtuales", pero el costo de hacerlo significa que TCP no es tan adecuado para los flujos multimedia digitales, donde el uso eficaz del ancho de banda es más importante que la pérdida ocasional de paquetes.

Cuando una dirección URL especifica "mms://", el lector intenta usar los siguientes protocolos para la entrega de datos, en el orden siguiente:

1.  RTSPU (RTSP mediante UDP)
2.  RTSPT (RTSP mediante TCP)
3.  MMSU (MMS con UDP)
4.  MMST (MMS mediante TCP)
5.  HTTP

HTTP es un protocolo unida basado en TCP y es el protocolo que usan los servidores web. El streaming con HTTP es menos eficaz que usar RTSP. Sin embargo, la mayoría de los firewalls están configurados para aceptar solicitudes HTTP, mientras que normalmente rechazan otros protocolos de streaming.

Servicios de Windows Media serie 9 de Microsoft Windows Server 2003 rechazará las solicitudes MMSU o MMST de un lector del SDK de formato multimedia de Windows, ya que RTSP es el protocolo de streaming preferido. Servicios de Windows Media versión 4.1 y anteriores no admiten RTSP. En este caso, el objeto de lector vuelve a MMSU o HTTP.

La suversión de protocolo no se aplica si el esquema de dirección URL proporciona un protocolo específico, como "rtspu://" para RTSPU o "https://" para HTTP. Si el esquema de dirección URL es "rtsp://", el lector intenta RTSPU y RTSPT, pero ningún otro.

Una vez que el lector abre un archivo, puede consultar qué protocolo está usando llamando al método [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname) en el lector. Mientras el contenido se transmite o descarga, este método devuelve el nombre en cuanto el contenido se almacena completamente en caché, el método **GetProtocolName** devuelve la cadena "Cache".

Para obtener los nombres de todos los protocolos de servidor de Windows Media que admite el lector, llame al método [**IWMReaderNetworkConfig::GetSupportedProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getsupportedprotocolname) en el lector. Puede deshabilitar uno o varios de los protocolos de la lista de suversión de protocolos del lector mediante la **interfaz IWMReaderNetworkConfig.** Por ejemplo, el método [**IWMReaderNetworkConfig::SetEnableTCP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenabletcp) habilita o deshabilita los protocolos basados en TCP, e [**IWMReaderNetworkConfig::SetEnableUDP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp) habilita o deshabilita los protocolos basados en UDP. Estos métodos solo se aplican a la suversión del protocolo; los protocolos siguen estando disponibles si el esquema de dirección URL contiene un protocolo específico. Normalmente no hay ninguna razón para deshabilitar ninguno de los protocolos usados en la suversión de protocolos. si lo hace, puede degradar el rendimiento. Sin embargo, puede ser útil para las pruebas.

 

 




