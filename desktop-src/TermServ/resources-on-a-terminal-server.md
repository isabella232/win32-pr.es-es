---
title: Recursos en un servidor host Escritorio remoto sesión de servidor
description: Varios usuarios pueden iniciar sesión simultáneamente en un único servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto) y compartir los recursos de hardware y software del servidor.
ms.assetid: ab193a9f-7424-42bf-8cea-28628096edc6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ba87ea7569b8ef9daeccb54890bb8882d423621b414fdd8df28c0c4e67b750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009195"
---
# <a name="resources-on-a-remote-desktop-session-host-server"></a>Recursos en un servidor host Escritorio remoto sesión de servidor

En un Servicios de Escritorio remoto remoto, varios usuarios pueden iniciar sesión simultáneamente en un único servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) (anteriormente conocido como servidor terminal). Por lo tanto, los usuarios comparten los recursos de hardware y software del servidor, lo que puede crear las siguientes áreas de contención:

-   Tiempo de CPU. Cada usuario tiene un entorno de escritorio y puede ejecutar todas las aplicaciones disponibles para ese escritorio. Sin embargo, todas las aplicaciones ejecutadas por todos los usuarios están contendiendo por los recursos centrales de CPU disponibles en el servidor host de sesión de Escritorio remoto. Si un usuario ejecuta una aplicación mal escrita que consume mucha CPU, es posible que otros usuarios experimente una pérdida visible de rendimiento.
-   Acceso al disco. Los usuarios se enfrentarán por el acceso a las aplicaciones y a los archivos de programa relacionados. Además, los usuarios se enfrentarán a los accesos de disco por parte del sistema operativo del servidor, como cargar archivos DLL o intercambiar memoria entre el archivo de paginación y la memoria física.
-   Memoria de acceso aleatorio (RAM). Cada aplicación ejecutada por cada usuario está contendiendo por los recursos de RAM disponibles en el servidor host de sesión de Escritorio remoto. Si un usuario ejecuta una aplicación que consume mucha memoria, otros usuarios podrían experimentar una pérdida de rendimiento.
-   Acceso a la red. El acceso a la red es esencial en un entorno de Servicios de Escritorio remoto porque toda la actividad de escritorio (salida gráfica y entrada de mouse/teclado) fluye a través de los vínculos de red entre el escritorio del cliente y el servidor. Además, las aplicaciones de los usuarios que se ejecutan en el servidor host de sesión de Escritorio remoto tienen que tener acceso a otros recursos de red.
-   Hardware del servidor. Los componentes de hardware, como CD-ROMs, unidades de disquete, puertos serie y puertos paralelos, a menudo se basan en el servidor, no en el cliente. Compartir estos componentes tradicionalmente no compartidos crea nuevas consideraciones para los usuarios y para las aplicaciones que acceden a estos componentes de hardware. Para obtener más información, vea [Directrices de hardware periférico.](peripheral-hardware-guidelines.md)
-   Acceso a objetos y recursos globales. En un Servicios de Escritorio remoto, los usuarios no ejecutan copias individuales de Windows: algunos de los módulos principales se clonan, pero los módulos restantes se comparten entre los usuarios. Por lo tanto, los usuarios compiten por el acceso al Registro, el archivo de paginación, los servicios del sistema y otros objetos y recursos globales.

Muchos de los puntos anteriores de contención se pueden mitigar si se dimensiona el servidor host de sesión de Escritorio remoto con suficientes recursos de CPU, memoria y disco para controlar la demanda del cliente. Por ejemplo, una configuración de varios procesadores puede maximizar la disponibilidad de la CPU. La disponibilidad de memoria se puede maximizar mediante la instalación de memoria física adicional (el aumento de los límites de memoria para las ediciones Enterprise, Datacenter o 64 bits de Windows Server puede ayudar). Por último, el rendimiento del acceso al disco se puede maximizar mediante la configuración de varios canales y la distribución de las cargas del sistema operativo y la aplicación entre diferentes unidades físicas. Configurar correctamente un servidor host de sesión de Escritorio remoto es un elemento crítico del rendimiento percibido de la aplicación.

Aunque el tamaño del hardware es una parte importante de la creación de un entorno Servicios de Escritorio remoto escalable, las consideraciones de software son igualmente importantes. De hecho, ajustar una aplicación a menudo puede hacer mucho para reducir la competencia de recursos y mejorar el rendimiento percibido de la aplicación.

Para obtener más información sobre el Servicios de Escritorio remoto, vea los temas siguientes:

-   [Servicios de Escritorio remoto de programación](terminal-services-programming-guidelines.md)
-   [Detección del Servicios de Escritorio remoto virtual](detecting-the-terminal-services-environment.md)
-   [Detectar si el rol Servicios de Escritorio remoto está instalado](detecting-whether-terminal-services-is-installed.md)
-   [Servicios de Escritorio remoto sesiones](terminal-services-sessions.md)

 

 




