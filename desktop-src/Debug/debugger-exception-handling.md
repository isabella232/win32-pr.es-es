---
description: El control del sistema de excepciones en modo de usuario proporciona compatibilidad con depuradores sofisticados.
ms.assetid: c45a7dc6-e6b2-4fc4-9522-12d96893f4c7
title: Control de excepciones del depurador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23595f68de31bb009a0b82d9257453ce7073eb489cc6a5b654ab4553ee60474
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103915"
---
# <a name="debugger-exception-handling"></a>Control de excepciones del depurador

El control del sistema de excepciones en modo de usuario proporciona compatibilidad con depuradores sofisticados. Si se depura el proceso en el que se produce una excepción, el sistema genera un evento de depuración. Si el depurador usa la [**función WaitForDebugEvent,**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) el evento de depuración hace que esa función vuelva con un puntero a una [**estructura DEBUG \_ EVENT.**](/windows/win32/api/minwinbase/ns-minwinbase-debug_event) Esta estructura contiene los identificadores de proceso y subproceso que el depurador puede usar para acceder al registro de contexto del subproceso. La estructura también contiene una estructura [**EXCEPTION \_ DEBUG \_ INFO**](/windows/win32/api/minwinbase/ns-minwinbase-exception_debug_info) que incluye una copia del registro de excepciones.

Cuando el sistema busca un controlador de excepciones, realiza dos intentos para notificar al depurador de un proceso. El primer intento de notificación proporciona al depurador una oportunidad para controlar el punto de interrupción o las excepciones de un solo paso. Esto se conoce como notificación *de primera oportunidad.* A continuación, el usuario puede emitir comandos del depurador para manipular el entorno del proceso antes de que se ejecuten los controladores de excepciones. El segundo intento de notificar al depurador solo se produce si el sistema no puede encontrar un controlador de excepciones basado en marco que controle la excepción. Esto se conoce como *notificación de última oportunidad.* Si el depurador no controla la excepción después de la notificación de última oportunidad, el sistema finaliza el proceso que se está depurando.

En cada intento de notificación, el depurador usa la [**función ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) para devolver el control al sistema. Antes de devolver el control, el depurador puede controlar la excepción y modificar el estado del subproceso según corresponda, o puede decidir no controlar la excepción. Mediante **ContinueDebugEvent**, el depurador puede indicar que ha administrado la excepción, en cuyo caso se restaura el estado de la máquina y la ejecución del subproceso continúa en el punto en el que se produjo la excepción. El depurador también puede indicar que no controló la excepción, lo que hace que el sistema continúe con la búsqueda de un controlador de excepciones.

 

 
