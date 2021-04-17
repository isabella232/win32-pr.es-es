---
description: Windows Installer se integra con la Directiva de restricción de software en Microsoft Windows XP.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Installer y Directiva de restricción de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678066"
---
# <a name="windows-installer-and-software-restriction-policy"></a>Windows Installer y Directiva de restricción de software

Windows Installer se integra con la Directiva de restricción de software en Microsoft Windows XP. La Directiva de restricción de software se puede configurar mediante la Directiva de grupo. La Directiva de restricción de software permite a un administrador restringir a los administradores y a los no administradores la ejecución de archivos basados en los criterios de ruta de acceso, zona URL, hash o publicador. La Directiva de restricción de software tiene dos niveles: no restringido y no permitido. La Windows Installer solo instala los paquetes que se pueden ejecutar en el nivel sin restricciones.

También se debe permitir que las revisiones o transformaciones se ejecuten en el nivel sin restricciones. Si un paquete, revisión o transformación está configurado para ejecutarse en un nivel diferente de Unrestricted, el Windows Installer muestra un mensaje de error y registra una entrada en el registro de eventos de la aplicación. La Directiva de restricción de software se evalúa la primera vez que se instala una aplicación, cuando se aplica una nueva revisión y cuando se vuelve a almacenar en caché el paquete de instalación.

Si un paquete, revisión o transformación está restringido, en el Windows Installer se muestra un mensaje de error y se escribe una entrada de [registro de eventos](event-logging.md) en el registro de eventos de la aplicación. La Directiva de restricción de software se evalúa la primera vez que se instala una aplicación, cuando se aplica una nueva revisión y cuando se vuelve a almacenar en caché el paquete de instalación.

Para obtener más información sobre la Directiva de restricción de software, consulte la documentación del producto y [Busque en el sitio de TechNet](https://www.microsoft.com/technet/sitemap.mspx).

 

 



