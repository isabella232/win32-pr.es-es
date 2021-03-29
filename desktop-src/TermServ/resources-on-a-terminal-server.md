---
title: Recursos en un servidor host de sesión Escritorio remoto
description: Varios usuarios pueden iniciar sesión simultáneamente en un único servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto), compartiendo los recursos de hardware y software del servidor.
ms.assetid: ab193a9f-7424-42bf-8cea-28628096edc6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e099787ae3d0acd9028405b244f7fbc2e2117e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776956"
---
# <a name="resources-on-a-remote-desktop-session-host-server"></a>Recursos en un servidor host de sesión Escritorio remoto

En un entorno de Servicios de Escritorio remoto, varios usuarios pueden iniciar sesión simultáneamente en un único servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto) (anteriormente conocido como servidor de Terminal Server). Por lo tanto, los usuarios comparten los recursos de hardware y software del servidor, lo que puede crear las siguientes áreas de contención:

-   Tiempo de CPU. Cada usuario tiene un entorno de escritorio y puede ejecutar cualquier aplicación que esté disponible para ese escritorio. Sin embargo, todas las aplicaciones ejecutadas por todos los usuarios están consiguiendo los recursos de CPU central disponibles en el servidor host de sesión de escritorio remoto. Si un usuario ejecuta una aplicación con un uso intensivo de la CPU y mal escrito, otros usuarios podrían experimentar una pérdida de rendimiento visible.
-   Acceso al disco. Los usuarios se compiten por el acceso a las aplicaciones y los archivos de programa relacionados. Además, los usuarios compiten por el acceso al disco mediante el sistema operativo del servidor, como la carga de archivos dll o el intercambio de memoria entre el archivo de paginación y la memoria física.
-   Memoria de acceso aleatorio (RAM). Cada aplicación ejecutada por cada usuario está intentando los recursos de RAM disponibles en el servidor host de sesión de escritorio remoto. Si un usuario ejecuta una aplicación con un uso intensivo de memoria, otros usuarios podrían experimentar una pérdida de rendimiento.
-   Acceso a la red. El acceso a la red es esencial en un entorno de Servicios de Escritorio remoto porque todas las actividades de escritorio (salida gráfica y entrada de mouse/teclado) fluyen a través de los vínculos de red entre el escritorio del cliente y el servidor. Además, las aplicaciones de los usuarios que se ejecutan en el servidor host de sesión de escritorio remoto compiten por el acceso a otros recursos de red.
-   Hardware del servidor. Los componentes de hardware, como los CD-ROM, las unidades de disquete, los puertos serie y los puertos paralelos suelen basarse en el servidor, no en el cliente. El uso compartido de estos componentes tradicionalmente no compartidos crea nuevas consideraciones para los usuarios y las aplicaciones que tienen acceso a estos componentes de hardware. Para obtener más información, consulte las [directrices de hardware de periféricos](peripheral-hardware-guidelines.md).
-   Acceso a objetos y recursos globales. En un entorno de Servicios de Escritorio remoto, los usuarios no ejecutan copias individuales de Windows; algunos de los módulos principales se clonan, pero el resto de los módulos se comparten entre los usuarios. Por lo tanto, los usuarios compiten por el acceso al registro, el archivo de paginación, los servicios del sistema y otros objetos y recursos globales.

Muchos de los puntos de contención anteriores se pueden mitigar mediante el ajuste de tamaño del servidor host de sesión de escritorio remoto con suficiente CPU, memoria y recursos de disco para controlar la demanda del cliente. Por ejemplo, una configuración de varios procesadores puede aumentar la disponibilidad de la CPU. La disponibilidad de memoria se puede maximizar mediante la instalación de memoria física adicional (el aumento de los límites de memoria para las ediciones Enterprise, Datacenter o 64-bit de Windows Server puede ser de ayuda). Por último, se puede maximizar el rendimiento del acceso al disco mediante la configuración de varios canales y la distribución de la carga del sistema operativo y de las aplicaciones en diferentes unidades físicas. Configurar correctamente un servidor host de sesión de escritorio remoto es un elemento crítico del rendimiento de la aplicación percibido.

Aunque el tamaño del hardware es una parte importante de la creación de un entorno de Servicios de Escritorio remoto escalable, las consideraciones sobre el software son igualmente importantes. De hecho, ajustar una aplicación a menudo puede hacer mucho para reducir la competencia de recursos y mejorar el rendimiento de la aplicación percibido.

Para obtener más información acerca del entorno de Servicios de Escritorio remoto, vea los temas siguientes:

-   [Instrucciones de programación de Servicios de Escritorio remoto](terminal-services-programming-guidelines.md)
-   [Detección del entorno de Servicios de Escritorio remoto](detecting-the-terminal-services-environment.md)
-   [Detectar si está instalado el rol de Servicios de Escritorio remoto](detecting-whether-terminal-services-is-installed.md)
-   [Sesiones de Servicios de Escritorio remoto](terminal-services-sessions.md)

 

 




