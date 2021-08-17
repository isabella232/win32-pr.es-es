---
description: Los contextos de activación son visibles a lo largo de todo el proceso.
ms.assetid: 6eda00d5-9dac-4267-bf61-b481814201f8
title: Subprocesos, procedimientos asincrónicos y mensajes de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529be75a3bc72679f44dfb69196f9487aa4f1de4f3cdbeada4ec89e26f05d646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141708"
---
# <a name="using-threads-asynchronous-procedures-and-window-messages"></a>Usar subprocesos, procedimientos asincrónicos y mensajes de ventana

Los contextos de activación son visibles a lo largo de todo el proceso. Sin embargo, las pilas de contexto de activación son por subproceso y dos subprocesos del mismo proceso pueden tener pilas de activación diferentes. [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) coloca automáticamente el contexto de activación actual en la parte superior de la pila de activación del nuevo subproceso. Esto puede facilitar la actualización del código existente para usar componentes en paralelo, ya que el nuevo subproceso se puede ejecutar inmediatamente en el contexto de activación actual.

Las llamadas a procedimiento asincrónico, las devoluciones de llamada de puerto de finalización y cualquier otra devolución de llamada de otros subprocesos obtienen automáticamente el contexto de activación del origen. Cuando se llama a la devolución de llamada, se limpia la pila de activación. Esto significa que la aplicación puede usar llamadas a procedimientos asincrónicos y devoluciones de llamada sin activar explícitamente ningún contexto, ya que la administración de contexto la realizará la infraestructura en paralelo subyacente. Para activar otros contextos durante una devolución de llamada o un subproceso nuevo, la aplicación puede realizar su propia administración de contexto. En este caso, el programa debe usar la secuencia adecuada de contexto de activación para activar funciones y desactivar funciones.

Los contextos de activación son neutros para subprocesos. La activación de un contexto solo cambia la pila del subproceso actual y no se puede activar un contexto entre subprocesos. El subproceso A no puede forzar un contexto en el subproceso B. Las funciones de la API de contexto de activación también son para subprocesos.

Cuando se usa [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) o [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para enviar un mensaje de ventana a otro procedimiento de ventana del proceso, el contexto de activación actual se activa antes de que el mensaje se pase al procedimiento de destino. El contexto de activación actual va junto con el mensaje. Esto garantiza que los mensajes que hacen referencia a objetos COM, nombres DLL u otros recursos en paralelo conservan su información de contexto correcta.

 

 
