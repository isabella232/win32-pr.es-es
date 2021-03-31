---
description: Los contextos de activación son visibles en todo el proceso.
ms.assetid: 6eda00d5-9dac-4267-bf61-b481814201f8
title: Subprocesos, procedimientos asincrónicos y mensajes de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e615eb9795ba32bcf4bd227a4933e890e9b89055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907830"
---
# <a name="using-threads-asynchronous-procedures-and-window-messages"></a>Usar subprocesos, procedimientos asincrónicos y mensajes de ventana

Los contextos de activación son visibles en todo el proceso. Sin embargo, las pilas de contexto de activación no son por subproceso y dos subprocesos en el mismo proceso pueden tener diferentes pilas de activación. [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) coloca automáticamente el contexto de activación actual en la parte superior de la pila de activación del subproceso. Esto puede facilitar la actualización del código existente para usar componentes en paralelo, ya que el nuevo subproceso se puede ejecutar inmediatamente en el contexto de activación actual.

Las llamadas a procedimientos asincrónicos, las devoluciones de llamada de puertos de finalización y cualquier otra devolución de llamada en otros subprocesos obtienen automáticamente el contexto de activación del origen. Cuando se llama a la devolución de llamada, se limpia la pila de activación. Esto significa que la aplicación puede utilizar llamadas a procedimientos asincrónicos y devoluciones de llamada sin activar explícitamente ningún contexto, ya que la administración del contexto se realizará mediante la infraestructura en paralelo subyacente. Para que otros contextos estén activos durante una devolución de llamada o un nuevo subproceso, la aplicación puede realizar su propia administración de contexto. En este caso, el programa debe usar la secuencia adecuada de las funciones de activación y desactivación del contexto de activación.

Los contextos de activación son independientes del subproceso. Al activar un contexto solo se cambia la pila del subproceso actual y no se puede activar un contexto entre subprocesos. El subproceso A no puede forzar un contexto en el subproceso B. Las funciones de la API de contexto de activación también tienen en cuenta el subprocesamiento.

Cuando se usa [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) o [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para enviar un mensaje de ventana a otro procedimiento de ventana del proceso, el contexto de activación actual se activa antes de que el mensaje se pase al procedimiento de destino. El contexto de activación actual se envía junto con el mensaje. Esto garantiza que los mensajes que hacen referencia a objetos COM, nombres DLL u otros recursos en paralelo conserven su información de contexto correcta.

 

 
