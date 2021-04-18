---
description: Aunque este mecanismo es suficiente para las aplicaciones sencillas, no puede admitir los requisitos de distribución de mensajes complejos de aplicaciones más avanzadas, como los que usan el modelo de interfaz de múltiples documentos (MDI).
ms.assetid: e4558e71-bbec-415a-a7c2-9025a4d6c474
title: Enlace de bloqueo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd098692784a662456c990a238bd309db0c321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715137"
---
# <a name="blocking-hook"></a>Enlace de bloqueo

Aunque este mecanismo es suficiente para las aplicaciones sencillas, no puede admitir los requisitos de distribución de mensajes complejos de aplicaciones más avanzadas, como los que usan el modelo de interfaz de múltiples documentos (MDI). Para estas aplicaciones, la aplicación puede instalar un enlace de bloqueo específico del subproceso. El proveedor de servicios llamará a este método en lugar del enlace de bloqueo predeterminado descrito en el anterior. Un proveedor de servicios debe recuperar un puntero al enlace de bloqueo por subproceso del \_32.dll Ws2 llamando a [**WPUQueryBlockingCallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback). Si la aplicación no ha instalado su propio enlace de bloqueo, se devolverá un puntero a la función de enlace de bloqueo predeterminada.

Un proveedor de servicios de Windows Sockets no puede suponer que un enlace de bloqueo proporcionado por la aplicación permita que el procesamiento de mensajes continúe como lo hace el enlace de bloqueo predeterminado. Algunas aplicaciones no pueden tolerar la posibilidad de que se produzcan mensajes reentrantes mientras una operación de bloqueo esté pendiente. Este tipo de función de enlace de bloqueo de una aplicación simplemente devolverá **false**. Si un proveedor de servicios depende de mensajes para su operación interna, puede ejecutar **PeekMessage**(hMyWnd...) antes de ejecutar el enlace de bloqueo de la aplicación para que pueda obtener sus propios mensajes sin afectar al resto del sistema.

No hay ningún enlace de bloqueo predeterminado instalado en las versiones preferentes multiproceso de Windows. Esto se debe a que otros procesos no se bloquearán si una sola aplicación está esperando a que se complete una operación (y, por tanto, no llama a **PeekMessage** o a **GetMessage** , lo que hace que la aplicación produzca el procesador en ventanas no adelantadas). Cuando el proveedor de servicios llama a [**WPUQueryBlockingCallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback) , se devolverá un puntero nulo que indica que el proveedor va a utilizar funciones de bloqueo del sistema operativo nativo. Sin embargo, para mantener la compatibilidad con versiones anteriores, un enlace de bloqueo proporcionado por la aplicación todavía se puede instalar por subproceso en Windows.

El proveedor de servicios Winsock llama al enlace de bloqueo solo si se cumplen todas las condiciones siguientes: la rutina es una que se define como capaz de bloquearse, el socket especificado es un socket de bloqueo y la solicitud no se puede completar inmediatamente. Si solo se usan Sockets sin bloqueos y [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) / [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) en lugar de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) , no se llamará nunca al enlace de bloqueo.

> [!Note]  
> Si, durante el tiempo que se usa pseudoblocking para bloquear un subproceso, se recibe un mensaje de Windows para el subproceso, existe el riesgo de que el subproceso intente emitir otra llamada Winsock. Debido a la dificultad de administrar esta condición de forma segura, la especificación 1,1 de Windows Sockets no permite este comportamiento. No se permite que un subproceso determinado realice varias llamadas a función Winsock anidadas. Solo se permite una llamada de función pendiente para un subproceso determinado. Cualquier llamada de función Winsock anidada produce un error WSAEINPROGRESS. Se debe resaltar que esta restricción se aplica a las operaciones de bloqueo y de no bloqueo, pero solo en entornos de Windows Sockets 1,1. Hay algunas excepciones a esta regla, incluidas dos funciones que permiten que una aplicación determine si una operación de pseudoblocking es de hecho en curso, y para cancelar esta operación si es necesario. Se describen a continuación.

 

 

 
