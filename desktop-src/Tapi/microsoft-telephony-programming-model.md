---
description: El modelo de programación de telefonía de Microsoft abstrae el control de comunicaciones del control de dispositivos, lo que libera a las aplicaciones de usuario final y a los fabricantes de dispositivos de la necesidad de marchar en el paso de bloqueo.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Modelo de programación de telefonía de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33407069c8ff489006c3cb85e03b676126eca1abedf484d9d1bb5b1305677a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518654"
---
# <a name="microsoft-telephony-programming-model"></a>Modelo de programación de telefonía de Microsoft

El modelo de programación de telefonía de Microsoft abstrae el control de comunicaciones del control de dispositivos, lo que libera a las aplicaciones de usuario final y a los fabricantes de dispositivos de la necesidad de marchar en el paso de bloqueo. Con este modelo, una aplicación de servidor o usuario final no requiere información detallada sobre el control de dispositivos y el dispositivo no necesita adaptarse a la aplicación. Las aplicaciones y los dispositivos pueden experimentar innovación y cambios sin que los clientes se desatenten unos a otros.

En el diagrama siguiente se muestra cómo se logra esta abstracción.

![cómo tapi abstrae el control de comunicaciones del control de dispositivos](images/tapicomp.png)

Estos componentes se pueden ver como repositorios de conocimientos especializados. La aplicación Interfaz de programación de aplicaciones de telefonía (TAPI) conoce las necesidades del usuario, el archivo DLL de TAPI y TAPISRV entienden la telefonía general y los proveedores de servicios (TSP y MSP) conocen el control detallado del dispositivo. Los escritores de aplicaciones y los fabricantes de dispositivos solo requieren un conocimiento general de los requisitos de los demás.

-   Una aplicación carga el archivo DLL de TAPI en su espacio de proceso y usa TAPI para comunicar las necesidades.
-   TAPI establece una comunicación de vínculo RPC con el servidor TAPI.
-   Además, TAPI 3.x crea un objeto MSP y se comunica con él mediante un conjunto definido de comandos, la interfaz del proveedor de servicios multimedia (MSPI).
-   Cuando una aplicación llama a una operación TAPI, la biblioteca de vínculos dinámicos TAPI valida y serializa los parámetros y, a continuación, reenvía la información a TAPISRV.
-   TAPISRV realiza un seguimiento de los recursos de comunicaciones disponibles para la máquina local y las interfaces con los proveedores de servicios de telefonía (TSP) mediante la interfaz del proveedor de servicios de telefonía (TSPI).
-   Las comunicaciones entre un TSP y un MSP tienen lugar mediante una conexión virtual que pasa a través de la DLL de TAPI y TAPISRV.
-   El par TSP/MSP proporciona información sobre el estado y las funcionalidades del dispositivo e implementa los comandos específicos necesarios para una respuesta deseada.

El resultado de usar este modelo de programación es que las aplicaciones pueden omitir o ajustarse a los cambios del dispositivo y los nuevos dispositivos pueden ser útiles al instante en lugar de esperar a los cambios de base de código. La cuota de mercado potencial se expande tanto para los escritores de aplicaciones como para los fabricantes de dispositivos.

En los temas siguientes se describen los componentes de telefonía de Microsoft con más detalle:

-   [Aplicaciones TAPI](tapi-applications.md)
-   [TAPI DLL](tapi-dll.md)
-   [Servidor TAPI](tapi-server.md)
-   [Proveedores de servicios](service-providers.md)
-   [Modelo sincrónico/asincrónico](synchronous-asynchronous-model.md)
-   [Estructuras de datos TAPI](tapi-data-structures.md)
-   [Niveles de servicio de TAPI](tapi-levels-of-service.md)

 

 



