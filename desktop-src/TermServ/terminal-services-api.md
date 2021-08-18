---
title: Servicios de Escritorio remoto API
description: La API Servicios de Escritorio remoto es principalmente útil para aplicaciones cliente/servidor y aplicaciones para Servicios de Escritorio remoto administración.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbdaff1f09a0de3fad20f4de334af1030c52e16ef795b1ece51cdaead639825a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000115"
---
# <a name="remote-desktop-services-api"></a>Servicios de Escritorio remoto API

La mayoría de las aplicaciones se ejecutan sin modificaciones Servicios de Escritorio remoto entorno (anteriormente conocido como Terminal Services) y no necesitan usar la API Servicios de Escritorio remoto. La API Servicios de Escritorio remoto es principalmente útil para aplicaciones cliente/servidor y aplicaciones para Servicios de Escritorio remoto administración.

La API Servicios de Escritorio remoto es un conjunto de llamadas de función a Wtsapi32.dll. Para diseñar la aplicación para que se ejecute en entornos de Servicios de Escritorio remoto y no Servicios de Escritorio remoto, use la vinculación dinámica en tiempo de ejecución para comprobar la presencia de Wtsapi32.dll. Para obtener más información, [vea Vinculación en tiempo de ](run-time-linking-to-wtsapi32-dll.md)ejecución a Wtsapi32.dll.

La API Servicios de Escritorio remoto permite a las aplicaciones realizar las siguientes tareas en un Servicios de Escritorio remoto de trabajo:

-   [Servicios de Escritorio remoto Administration](terminal-services-administration.md), como enumerar y administrar servidores de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) (anteriormente conocidos como servidores de terminal server) en un dominio o enumerar y administrar sesiones y procesos en un servidor host de sesión de Escritorio remoto.
-   Mejorar las aplicaciones cliente/servidor en un entorno Servicios de Escritorio remoto cliente.
-   Usar [Servicios de Escritorio remoto virtuales para](terminal-services-virtual-channels.md) comunicarse entre los módulos de cliente y servidor de una aplicación.
-   [Establecer y recuperar Servicios de Escritorio remoto información de configuración de usuario específica](terminal-services-user-configuration.md).

 

 




