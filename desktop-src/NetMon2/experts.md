---
description: Un experto es una biblioteca de vínculos dinámicos (DLL) de Microsoft Win32 que analiza el tráfico de red recopilado por un proveedor de paquetes de red (NPP) y colocado en un archivo de captura.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2f4c3e34a9f6b8b36fdc6aa4793acfa5b652b9fa2c2117afc62943c0947af6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890925"
---
# <a name="expert"></a>Experto

Un experto es una biblioteca de vínculos dinámicos (DLL) de Microsoft Win32 que analiza el tráfico de red recopilado por un proveedor de paquetes de [*red*](n.md) (NPP) y colocado en un archivo de captura. Después de capturar y almacenar los datos en un archivo de captura, el experto trabaja con un analizador, también conocido como analizador de protocolos, para analizar los datos del archivo. Por ejemplo, puede examinar los fotogramas del archivo de captura y usar un analizador para reconocer [*protocolos*](p.md) como el bloque de mensajes del servidor (SMB) o el Protocolo de control de transmisión/Protocolo de Internet (TCP/IP).

Puede diseñar un experto para trabajar con todos los analizadores de Monitor de red y los analizadores que cree usted mismo.

Después de que una coincidencia solicitada de protocolos identifique un marco específico, el experto extrae datos del marco. Puede programar al experto para manipular información en datos utilizables que el Monitor de red Visor de eventos muestra.

Puede configurar un experto en tiempo de ejecución y, a continuación, usar Monitor de red guardar los datos de configuración de usuario para reutilizarlos con diferentes archivos de captura. Puede usar un experto para proporcionar datos de correlación y resoluciones personalizadas para los usuarios finales. Para obtener más información sobre la creación de información de configuración basada en HTML, vea [Página de referencia de eventos](event-reference-page.md).

Durante Monitor de red instalación, se instalan los siguientes archivos DLL expertos en el sub directory Experts:

-   Coalesce.dll
-   Propdist.dll
-   Protdist.dll
-   Resptime.dll
-   Tcpipe.dll
-   Topuser.dll

Cuando se inicia Monitor de red, la [**función DllMain**](dllmain-expert.md) compila todos los expertos en el subdirectorio experts. Cuando el usuario selecciona  **Expertos en el** menú Herramientas de la interfaz Monitor de red usuario, Monitor de red carga los archivos DLL expertos. Se llama al experto a través del punto [de entrada Registrar](register-expert.md) experto para proporcionar detalles básicos sobre el experto.

![network monitor experts (expertos en supervisión de red), cuadro de diálogo](images/expick.png)

Monitor de red llama a las siguientes funciones para administrar al experto:

-   [**DllMain**](dllmain-expert.md)
-   [**Registro de un experto**](register-expert.md)
-   [**Ejecutar**](run.md)
-   [**Configurar**](configure.md)

El experto debe implementar cada una de las funciones anteriores.

 

 



