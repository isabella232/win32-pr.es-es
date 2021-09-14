---
description: El SDK Monitor de red incluye las funciones y el código de ejemplo que necesita para crear expertos. Sin embargo, también puede usar herramientas existentes, incluido un editor de cuadros de diálogo.
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: Programación de un experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362137"
---
# <a name="programming-an-expert"></a>Programación de un experto

El SDK Monitor de red incluye las funciones y el código de ejemplo que necesita para crear expertos. Sin embargo, también puede usar herramientas existentes, incluido un editor de cuadros de diálogo.

## <a name="minimum-requirements-to-run-an-expert"></a>Requisitos mínimos para ejecutar un experto

En la tabla siguiente se enumeran los puntos de entrada de DLL y las funciones de expertos que debe usar para crear un experto.



| Nombre                                                 | Tipo               | ¿Necesario?                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [**DllMain**](dllmain-expert.md)                    | Función de entrada dll | Sí                                             |
| [**Registro de un experto**](register-expert.md)           | Función de entrada dll | Sí                                             |
| [**Ejecutar**](run.md)                                   | Función de entrada dll | Sí                                             |
| [**Configuración**](configure.md)                       | Función de entrada dll | Solo si el experto proporciona la configuración del usuario. |
| [**ExpertIndicateStatus**](expertindicatestatus.md) | Función expert    | Sí                                             |
| [**ExpertSubmitEvent**](expertsubmitevent.md)       | Función expert    | Sí                                             |



 

Revise los temas de referencia de expertos y analizadores del SDK de Monitor de red para actualizar el código fuente y, a continuación, use el código de ejemplo y los procedimientos que se proporcionan en estos temas:

-   [Creación de un experto](building-an-expert.md)
-   [Instalación de un experto](installing-an-expert-to-network-monitor-2-1.md)
-   [Depuración de un experto](debugging-an-expert.md)

Los archivos DLL expertos requieren la convención de llamada de C, no C++, porque las funciones se llaman a través de punteros de función mediante una superposición. A través de un conjunto de funciones especializadas de expertos, el experto tiene acceso a los fotogramas de la captura. El experto puede usar la mayoría de Monitor de red API para manipular los datos devueltos. Cuando un experto encuentra información para enviar al usuario, empaqueta la información en una estructura de datos de eventos y la envía a Monitor de red, que luego muestra la información en una ventana de salida de expertos. El experto debe actualizar periódicamente Monitor de red información de estado de finalización porcentual, que proporciona la [**función ExpertIndicateStatus.**](expertindicatestatus.md)

Las funciones exportadas del experto se llaman de la siguiente manera:

-   Cuando Monitor de red la lista de expertos que se va a presentar al usuario, Monitor de red llama a [**la función Register Expert.**](register-expert.md)
-   Después de llamar a **Register**, si el experto es configurable, Monitor de red llama a la [**función Configure.**](configure.md)
-   Cuando el Monitor de red hace clic en **Ejecutar** experto, Monitor de red llama a la [**función Run.**](run.md)

Cuando los expertos analizan los fotogramas solicitados y encuentran un problema, usan [**ExpertSubmitEvent**](expertsubmitevent.md) para enviar un evento que contiene información sobre el problema. Monitor de red distribuye el evento a la versión estándar (compartida) Visor de eventos (si el experto se registra para él) a una Visor de eventos.

 

 



