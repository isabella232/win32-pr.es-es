---
description: El modelo de programación de telefonía de Microsoft abstrae el control de comunicaciones desde el control de dispositivos, liberando a las aplicaciones de usuario final y a los fabricantes de dispositivos de la necesidad de marzo en lógico.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Modelo de programación de telefonía de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efb8947f3b428ab4a252301e3fdd5f94e29f6ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686478"
---
# <a name="microsoft-telephony-programming-model"></a>Modelo de programación de telefonía de Microsoft

El modelo de programación de telefonía de Microsoft abstrae el control de comunicaciones desde el control de dispositivos, liberando a las aplicaciones de usuario final y a los fabricantes de dispositivos de la necesidad de marzo en lógico. Con este modelo, una aplicación de servidor o de usuario final no necesita información detallada sobre el control de dispositivo y no es necesario que el dispositivo esté adaptado a la aplicación. Las aplicaciones y los dispositivos pueden someterse a la innovación y al cambio sin necesidad de representar a los clientes.

En el diagrama siguiente se muestra cómo se realiza esta abstracción.

![Cómo abstrae TAPI el control de comunicaciones del control de dispositivo](images/tapicomp.png)

Estos componentes se pueden ver como repositorios de conocimientos especializados. La aplicación de interfaz de programación de aplicaciones de telefonía (TAPI) conoce las necesidades de los usuarios, la DLL de TAPI y TAPISRV comprenden la telefonía general y los proveedores de servicios (TSP y MSP) saben el control detallado del dispositivo. Los escritores de aplicaciones y los fabricantes de dispositivos solo necesitan conocimientos generales de los requisitos de los demás.

-   Una aplicación carga el archivo DLL de TAPI en su espacio de proceso y usa TAPI para comunicar las necesidades.
-   TAPI establece comunicaciones de vínculo RPC con el servidor TAPI.
-   Además, TAPI 3. x crea un objeto MSP y se comunica con él mediante un conjunto definido de comandos, la interfaz del proveedor de servicios multimedia (MSPI).
-   Cuando una aplicación llama a una operación de TAPI, la biblioteca de vínculos dinámicos TAPI valida y calcula las referencias de los parámetros y, a continuación, reenvía la información a TAPISRV.
-   TAPISRV realiza un seguimiento de los recursos de comunicaciones disponibles en el equipo local e interactúa con los proveedores de servicios de telefonía (profesionales) mediante la interfaz del proveedor de servicios de telefonía (TSPI).
-   Las comunicaciones entre un TSP y un MSP tienen lugar mediante una conexión virtual que pasa a través de la DLL de TAPI y TAPISRV.
-   El par TSP/MSP proporciona información sobre el estado y las capacidades del dispositivo e implementa los comandos específicos necesarios para una respuesta deseada.

El resultado de utilizar este modelo de programación es que las aplicaciones pueden omitir o ajustarse a los cambios del dispositivo y los nuevos dispositivos pueden ser útiles al instante en lugar de esperar a que se produzcan cambios en el código base. La cuota de mercado potencial se expande para los escritores de aplicaciones y los fabricantes de dispositivos.

En los temas siguientes se describen los componentes de telefonía de Microsoft con más detalle:

-   [Aplicaciones TAPI](tapi-applications.md)
-   [DLL DE TAPI](tapi-dll.md)
-   [Servidor TAPI](tapi-server.md)
-   [Proveedores de servicios](service-providers.md)
-   [Modelo sincrónico/asincrónico](synchronous-asynchronous-model.md)
-   [Estructuras de datos TAPI](tapi-data-structures.md)
-   [Niveles de servicio de TAPI](tapi-levels-of-service.md)

 

 



