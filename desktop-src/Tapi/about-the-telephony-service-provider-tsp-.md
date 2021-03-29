---
description: Un proveedor de servicios de telefonía (TSP) TAPI es una biblioteca de vínculos dinámicos (DLL) que admite el control de los dispositivos de comunicaciones a través de un conjunto de funciones de servicio exportadas.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: Acerca del proveedor de servicios de telefonía (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809242"
---
# <a name="about-the-telephony-service-provider-tsp"></a>Acerca del proveedor de servicios de telefonía (TSP)

\[ Los profesionales H323 y IPConf no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Un proveedor de servicios de telefonía (TSP) TAPI es una biblioteca de vínculos dinámicos (DLL) que admite el control de los dispositivos de comunicaciones a través de un conjunto de funciones de servicio exportadas. Una aplicación TAPI usa comandos estandarizados, TAPI pasa al proveedor de servicios de telefonía y el TSP controla los comandos específicos que se deben intercambiar con el dispositivo.

En las siguientes secciones se describen brevemente los profesionales proporcionados con Microsoft Windows:

-   [TSP H323](h323-tsp.md)
-   [IPConf TSP](ipconf-tsp.md)
-   [Proveedor de dispositivos de modo kernel (TSP)](kernel-mode-device-driver-tsp.md)
-   [TSP de proxy NDIS](ndis-proxy-tsp.md)
-   [TSP remoto](remote-tsp.md)
-   [TSP de terceros](third-party-tsp.md)
-   [TSP de Unimodem](unimodem-tsp.md)

Para obtener información detallada, consulte el kit de recursos del sistema operativo de destino. Normalmente, el fabricante proporcionará profesionales de terceros para dispositivos de comunicaciones especializados y se instalará con el dispositivo.

En los temas siguientes se describe cómo crear un TSP que funcione correctamente en el entorno de telefonía de Microsoft y cómo crear un par de TSP/MSP:

-   [Interfaz del proveedor de servicios de telefonía (TSPI)](telephony-service-provider-interface-tspi-.md)
-   [Referencia de TSPI](tspi-reference.md)
-   [Proveedores de servicios multimedia](./media-service-providers-start-page.md)

> [!Note]  
> Un TSP es un archivo DLL creado por el usuario. Si va a crear un TSP para una plataforma de Windows de 64 bits, debe compilarlo como DLL o dll de 64 bits.

 

 

 
