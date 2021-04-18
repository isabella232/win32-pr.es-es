---
title: Acerca de las extensiones de NPS
description: En esta sección se describe cómo implementar archivos DLL para ampliar la funcionalidad de NPS. Describe la interacción entre NPS y los archivos dll, y presenta algunas consideraciones de diseño relacionadas con los archivos dll.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05878a5243774046c1ca052052d59be9378483d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665858"
---
# <a name="about-nps-extensions"></a>Acerca de las extensiones de NPS

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

En esta sección se describe cómo implementar archivos DLL para ampliar la funcionalidad de NPS. Describe la interacción entre NPS y los archivos dll, y presenta algunas consideraciones de diseño relacionadas con los archivos dll.

NPS proporciona dos puntos de extensión, uno para la autenticación y el otro para la autorización. La autenticación se refiere a la comprobación de la identidad del usuario. La autorización se refiere a determinar qué servicios debe proporcionar la red al usuario. Los dos puntos de extensión corresponden a los archivos dll de extensión de autenticación y dll de extensión de autorización. Cada punto de extensión puede admitir varios archivos dll.

NPS proporciona servicios de autenticación y autorización. NPS llama a los archivos dll de extensión de autenticación antes de la autenticación y autorización de NPS integrada. Se llama a los archivos dll de extensión de autorización después de la autenticación y autorización de NPS.

En el diagrama siguiente se ilustra el flujo de paquetes a través de un servidor RADIUS NPS que se expande mediante el uso de archivos dll de extensión.

![proceso de autenticación y autorización de NPS](images/ias03.png)

Si un archivo DLL de extensión de autenticación devuelve ACCEPT, el paquete omite la autenticación NPS y va directamente a la autorización NPS.

> [!Note]  
> Cuando hay varios archivos dll de extensión de autenticación, es posible que también se omita el resto de los archivos dll de extensión. Para obtener más información, consulte [configuración de los archivos dll de extensión](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) .

 

Si un archivo DLL de extensión de autenticación devuelve CONTINUE, el paquete va a la autenticación NPS y, a continuación, a la autorización NPS.

> [!Note]  
> Cuando hay varios archivos dll de extensión de autenticación, el resto de los archivos dll de extensión de autenticación se invocan antes de la autenticación NPS.

 

En los temas siguientes se describen con más detalle los archivos dll de extensión:

-   [Configuración de los archivos dll de extensión](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [Invocar los archivos dll de extensión](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [Atributos de identificación de usuario](/windows/desktop/Nps/ias-user-identification-attributes)

 

 