---
description: El control del sistema de las excepciones de modo de usuario proporciona compatibilidad con depuradores sofisticados.
ms.assetid: c45a7dc6-e6b2-4fc4-9522-12d96893f4c7
title: Control de excepciones del depurador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aff6d566e8798aaf4f3113ce6d8f44a3bc71ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495809"
---
# <a name="debugger-exception-handling"></a>Control de excepciones del depurador

El control del sistema de las excepciones de modo de usuario proporciona compatibilidad con depuradores sofisticados. Si se está depurando el proceso en el que se produce una excepción, el sistema genera un evento de depuración. Si el depurador utiliza la función [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) , el evento de depuración hace que la función devuelva un puntero a una estructura de [**\_ eventos de depuración**](/windows/win32/api/minwinbase/ns-minwinbase-debug_event) . Esta estructura contiene los identificadores de proceso y de subproceso que el depurador puede utilizar para tener acceso al registro de contexto del subproceso. La estructura también contiene una estructura de [**\_ \_ información de depuración de excepción**](/windows/win32/api/minwinbase/ns-minwinbase-exception_debug_info) que incluye una copia del registro de excepciones.

Cuando el sistema busca un controlador de excepciones, realiza dos intentos de notificar al depurador de un proceso. El primer intento de notificación proporciona al depurador la oportunidad de controlar las excepciones de un punto de interrupción o de un solo paso. Esto se conoce como *notificación de primera oportunidad*. Después, el usuario puede emitir comandos del depurador para manipular el entorno del proceso antes de que se ejecuten los controladores de excepciones. El segundo intento de notificar al depurador solo se produce si el sistema no puede encontrar un controlador de excepciones basado en fotogramas que controle la excepción. Esto se conoce como *notificación de última oportunidad*. Si el depurador no controla la excepción después de la notificación de última oportunidad, el sistema finaliza el proceso que se está depurando.

En cada intento de notificación, el depurador utiliza la función [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) para devolver el control al sistema. Antes de devolver el control, el depurador puede controlar la excepción y modificar el estado del subproceso según corresponda, o puede optar por no controlar la excepción. Con **ContinueDebugEvent**, el depurador puede indicar que se ha controlado la excepción, en cuyo caso se restaura el estado del equipo y se continúa la ejecución del subproceso en el punto en el que se produjo la excepción. El depurador también puede indicar que no controló la excepción, lo que hace que el sistema continúe su búsqueda para un controlador de excepciones.

 

 
