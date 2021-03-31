---
title: API de Servicios de Escritorio remoto
description: La API de Servicios de Escritorio remoto es especialmente útil para las aplicaciones cliente/servidor y para la administración de Servicios de Escritorio remoto.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5aa187378625242463ea91151a6961b08d2a77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903352"
---
# <a name="remote-desktop-services-api"></a>API de Servicios de Escritorio remoto

La mayoría de las aplicaciones se ejecutan sin modificaciones en un entorno Servicios de Escritorio remoto (antes conocido como Terminal Services) y no necesitan usar la API de Servicios de Escritorio remoto. La API de Servicios de Escritorio remoto es especialmente útil para las aplicaciones cliente/servidor y para la administración de Servicios de Escritorio remoto.

La API de Servicios de Escritorio remoto es un conjunto de llamadas de función en Wtsapi32.dll. Para diseñar la aplicación de forma que se ejecute en entornos Servicios de Escritorio remoto y no Servicios de Escritorio remoto, utilice la vinculación dinámica en tiempo de ejecución para comprobar la presencia de Wtsapi32.dll. Para obtener más información, vea [vinculación en tiempo de ejecución a Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

La API de Servicios de Escritorio remoto permite a las aplicaciones realizar las siguientes tareas en un entorno de Servicios de Escritorio remoto:

-   [Servicios de escritorio remoto administración](terminal-services-administration.md), como la enumeración y la escritorio remoto administración de los servidores de host de sesión de escritorio remoto (host de sesión de RD) (anteriormente conocidos como servidores de Terminal Server) en un dominio o la enumeración y administración de sesiones y procesos en un servidor host de sesión de escritorio remoto.
-   Mejorar las aplicaciones cliente/servidor en un entorno de Servicios de Escritorio remoto.
-   El uso de [servicios de escritorio remoto canales virtuales](terminal-services-virtual-channels.md) para comunicarse entre los módulos de cliente y servidor de una aplicación.
-   [Establecer y recuperar servicios de escritorio remoto información de configuración específica del usuario](terminal-services-user-configuration.md).

 

 




