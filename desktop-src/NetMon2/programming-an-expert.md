---
description: El SDK de Monitor de red incluye las funciones y el código de ejemplo que necesita para crear expertos. Sin embargo, también puede usar las herramientas existentes, incluido un editor de cuadros de diálogo.
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: Programar un experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156308"
---
# <a name="programming-an-expert"></a>Programar un experto

El SDK de Monitor de red incluye las funciones y el código de ejemplo que necesita para crear expertos. Sin embargo, también puede usar las herramientas existentes, incluido un editor de cuadros de diálogo.

## <a name="minimum-requirements-to-run-an-expert"></a>Requisitos mínimos para ejecutar un experto

En la tabla siguiente se enumeran los puntos de entrada de DLL y las funciones de experto que debe usar para crear un experto.



| Nombre                                                 | Tipo               | ¿Necesario?                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [**DllMain**](dllmain-expert.md)                    | Función de entrada DLL | Sí                                             |
| [**Registrar experto**](register-expert.md)           | Función de entrada DLL | Sí                                             |
| [**Ejecutar**](run.md)                                   | Función de entrada DLL | Sí                                             |
| [**Configuración**](configure.md)                       | Función de entrada DLL | Solo si el experto proporciona la configuración de usuario. |
| [**ExpertIndicateStatus**](expertindicatestatus.md) | Función experta    | Sí                                             |
| [**ExpertSubmitEvent**](expertsubmitevent.md)       | Función experta    | Sí                                             |



 

Revise los temas de referencia de expertos y del analizador en el Monitor de red SDK para actualizar el código fuente y, a continuación, use el código de ejemplo y los procedimientos proporcionados en estos temas:

-   [Creación de un experto](building-an-expert.md)
-   [Instalación de un experto](installing-an-expert-to-network-monitor-2-1.md)
-   [Depuración de un experto](debugging-an-expert.md)

Los archivos dll expertos requieren la Convención de llamada C, no la de C++, porque las funciones se llaman a través de punteros de función mediante una superposición. A través de un conjunto de funciones expertas especializadas, el experto tiene acceso a los fotogramas de la captura. El experto puede usar la mayoría de las API de Monitor de red para manipular los datos devueltos. Cuando un experto encuentra información para enviar al usuario, empaqueta la información en una estructura de datos de eventos y la envía a Monitor de red, que muestra la información en una ventana de salida experta. El experto debe actualizar periódicamente Monitor de red con información de estado de finalización de porcentaje, proporcionada por la función [**ExpertIndicateStatus**](expertindicatestatus.md) .

A las funciones exportadas del experto se les llama de la manera siguiente:

-   Cuando Monitor de red está creando la lista de expertos que va a presentar al usuario, Monitor de red llama a la función [**registrar experto**](register-expert.md) .
-   Después de la llamada a **Register**, si el experto es configurable, monitor de red llama a la función [**Configure**](configure.md) .
-   Cuando el usuario Monitor de red hace clic en **Ejecutar experto**, monitor de red llama a la función [**Ejecutar**](run.md) .

Cuando los expertos analizan los fotogramas solicitados y encuentran un problema, usan [**ExpertSubmitEvent**](expertsubmitevent.md) para enviar un evento que contiene información sobre el problema. Monitor de red distribuye el evento al Visor de eventos estándar (compartido) o (si el experto lo registra) en una Visor de eventos privada.

 

 



