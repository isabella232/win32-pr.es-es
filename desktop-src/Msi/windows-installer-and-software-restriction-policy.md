---
description: Windows El instalador se integra con la directiva de restricción de software en Microsoft Windows XP.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Instalador y directiva de restricción de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069578"
---
# <a name="windows-installer-and-software-restriction-policy"></a>Windows Instalador y directiva de restricción de software

Windows El instalador se integra con la directiva de restricción de software en Microsoft Windows XP. La directiva de restricción de software se puede configurar a través de la directiva de grupo. La directiva de restricción de software permite que un administrador restrinja tanto a los administradores como a los no administradores la ejecución de archivos en función de la ruta de acceso, la zona url, el hash o los criterios del publicador. La directiva de restricción de software tiene dos niveles: sin restricciones y no permitido. El Windows instala solo los paquetes que se pueden ejecutar en el nivel sin restricciones.

También se debe permitir que las revisiones o transformaciones se ejecuten en el nivel sin restricciones. Si un paquete, una revisión o una transformación están configurados para ejecutarse en un nivel diferente de sin restricciones, el instalador de Windows muestra un mensaje de error y registra una entrada en el registro de eventos de la aplicación. La directiva de restricción de software se evalúa la primera vez que se instala una aplicación, cuando se aplica una nueva revisión y cuando se vuelve a almacenar en caché el paquete de instalación.

Si se restringe un paquete, una revisión o una transformación, el instalador de Windows muestra un mensaje de error y escribe una entrada [registro](event-logging.md) de eventos en el registro de eventos de la aplicación. La directiva de restricción de software se evalúa la primera vez que se instala una aplicación, cuando se aplica una nueva revisión y cuando se vuelve a almacenar en caché el paquete de instalación.

Para obtener más información sobre la directiva de restricción de software, consulte la documentación del producto y [busque en el sitio de TechNet](https://www.microsoft.com/technet/sitemap.mspx).

 

 



