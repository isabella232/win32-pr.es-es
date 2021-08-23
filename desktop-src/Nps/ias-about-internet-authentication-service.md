---
title: Acerca de las extensiones nps
description: En esta sección se describe cómo implementar archivos DLL para ampliar la funcionalidad de NPS. Describe la interacción entre NPS y los archivos DLL, y presenta algunas consideraciones de diseño con respecto a los archivos DLL.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 204fff8d97548e79eed3e317b3e14291e7288b55c51384c25ef8b912ad2d6095
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799474"
---
# <a name="about-nps-extensions"></a>Acerca de las extensiones nps

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se cambió a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

En esta sección se describe cómo implementar archivos DLL para ampliar la funcionalidad de NPS. Describe la interacción entre NPS y los archivos DLL, y presenta algunas consideraciones de diseño con respecto a los archivos DLL.

NPS proporciona dos puntos de extensión, uno para la autenticación y otro para la autorización. La autenticación hace referencia a la comprobación de la identidad del usuario. La autorización hace referencia a determinar qué servicios debe proporcionar la red al usuario. Los dos puntos de extensión corresponden a los archivos DLL de extensión de autenticación y a los archivos DLL de extensión de autorización. Cada punto de extensión puede admitir varios archivos DLL.

NPS proporciona servicios de autenticación y autorización. NPS llama a los archivos DLL de extensión de autenticación antes de la autenticación y autorización de NPS integradas. Se llama a los archivos DLL de extensión de autorización después de la autenticación y autorización de NPS.

En el diagrama siguiente se muestra el flujo de paquetes a través de un servidor NPS RADIUS que se expande mediante archivos DLL de extensión.

![Proceso de autenticación y autorización de nps](images/ias03.png)

Si un archivo DLL de extensión de autenticación devuelve ACCEPT, el paquete omite la autenticación nps y va directamente a la autorización de NPS.

> [!Note]  
> Cuando hay varios archivos DLL de extensión de autenticación, también se pueden omitir el resto de los archivos DLL de extensión. Consulte [Configuración de los archivos DLL de extensión](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) para obtener más información.

 

Si un archivo DLL de extensión de autenticación devuelve CONTINUE, el paquete pasa a la autenticación nps y, a continuación, a la autorización de NPS.

> [!Note]  
> Cuando hay varios archivos DLL de extensión de autenticación, el resto de los archivos DLL de extensión de autenticación se invocan antes de la autenticación de NPS.

 

En los temas siguientes se describen los archivos DLL de extensión con más detalle:

-   [Configuración de los archivos DLL de extensión](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [Invocación de los archivos DLL de extensión](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [Atributos de identificación de usuario](/windows/desktop/Nps/ias-user-identification-attributes)

 

 