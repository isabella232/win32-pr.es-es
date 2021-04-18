---
description: Un experto es una biblioteca de vínculos dinámicos (DLL) de Microsoft Win32 que analiza el tráfico de red recopilado por un proveedor de paquetes de red (NPP) y colocado en un archivo de captura.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf5fc0096b15d590bf70859443667f2d9969f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666295"
---
# <a name="expert"></a>Experto

Un experto es una biblioteca de vínculos dinámicos (DLL) de Microsoft Win32 que analiza el tráfico de red recopilado por un [*proveedor de paquetes de red*](n.md) (NPP) y colocado en un archivo de captura. Una vez que los datos se capturan y almacenan en un archivo de captura, el experto trabaja con un analizador, también denominado analizador de protocolos, para analizar los datos del archivo. Por ejemplo, puede examinar los fotogramas del archivo de captura y usar un [*analizador*](p.md) para reconocer protocolos como el bloque de mensajes del servidor (SMB) o el protocolo de control de transmisión/Protocolo de Internet (TCP/IP).

Puede diseñar un experto para que funcione con todos los analizadores de Monitor de red y los analizadores que cree usted mismo.

Después de que una coincidencia solicitada de protocolos identifique un marco específico, el experto extrae los datos del marco. Puede programar el experto para manipular la información en datos que se pueden usar que muestra el Monitor de red Visor de eventos.

Puede configurar un experto en tiempo de ejecución y, a continuación, usar Monitor de red para guardar los datos de configuración de usuario para su reutilización con diferentes archivos de captura. Puede usar un experto para proporcionar datos de correlación y resoluciones personalizadas para los usuarios finales. Para obtener más información sobre la creación de información de configuración basada en HTML, vea [Página referencia de eventos](event-reference-page.md).

Durante la instalación de Monitor de red, se instalan los siguientes archivos dll de expertos en el subdirectorio Experts:

-   Coalesce.dll
-   Propdist.dll
-   Protdist.dll
-   Resptime.dll
-   Tcpipe.dll
-   Topuser.dll

Al iniciar Monitor de red, la función [**DllMain**](dllmain-expert.md) crea todos los expertos en el subdirectorio Experts. Cuando el usuario selecciona **expertos** en el menú **herramientas** de la interfaz de usuario de monitor de red, monitor de red carga los archivos dll de expertos. Se llama al experto a través del punto de entrada del [experto de registro](register-expert.md) para proporcionar los detalles básicos sobre el experto.

![cuadro de diálogo expertos de monitor de red](images/expick.png)

Monitor de red llama a las siguientes funciones para administrar el experto:

-   [**DllMain**](dllmain-expert.md)
-   [**Registrar experto**](register-expert.md)
-   [**Ejecutar**](run.md)
-   [**Configuración**](configure.md)

El experto debe implementar cada una de las funciones anteriores.

 

 



