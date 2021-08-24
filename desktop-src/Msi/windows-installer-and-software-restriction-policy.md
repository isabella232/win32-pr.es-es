---
description: Windows El instalador se integra con la directiva de restricción de software en Microsoft Windows XP.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Instalador y directiva de restricción de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e96d1c422b38fd82110cac34953f24be39909eeb64fa2236d3a993925a55c6e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786565"
---
# <a name="windows-installer-and-software-restriction-policy"></a>Windows Instalador y directiva de restricción de software

Windows El instalador se integra con la directiva de restricción de software en Microsoft Windows XP. La directiva de restricción de software se puede configurar a través de la directiva de grupo. La directiva de restricción de software permite a un administrador restringir tanto a los administradores como a los no administradores la ejecución de archivos en función de los criterios de ruta de acceso, zona de dirección URL, hash o publicador. La directiva de restricción de software tiene dos niveles: sin restricciones y no permitido. El Windows instalación solo instala paquetes que se pueden ejecutar en el nivel sin restricciones.

Las revisiones o transformaciones también deben poder ejecutarse en el nivel sin restricciones. Si un paquete, una revisión o una transformación están configurados para ejecutarse en un nivel distinto de sin restricciones, el instalador de Windows muestra un mensaje de error y registra una entrada en el registro de eventos de la aplicación. La directiva de restricción de software se evalúa la primera vez que se instala una aplicación, cuando se aplica una nueva revisión y cuando se vuelve a almacenar en caché el paquete de instalación.

Si un paquete, revisión o transformación está restringido, el instalador de [](event-logging.md) Windows muestra un mensaje de error y escribe una entrada de Registro de eventos en el registro de eventos de la aplicación. La directiva de restricción de software se evalúa la primera vez que se instala una aplicación, cuando se aplica una nueva revisión y cuando se vuelve a almacenar en caché el paquete de instalación.

Para obtener más información sobre la directiva de restricción de software, consulte la documentación del producto y [busque en el sitio de TechNet](https://www.microsoft.com/technet/sitemap.mspx).

 

 



