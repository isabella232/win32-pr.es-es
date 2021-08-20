---
description: Aunque este mecanismo es suficiente para aplicaciones sencillas, no puede admitir los complejos requisitos de distribución de mensajes de aplicaciones más avanzadas, como las que usan el modelo de interfaz de múltiples documentos (MDI).
ms.assetid: e4558e71-bbec-415a-a7c2-9025a4d6c474
title: Enlace de bloqueo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df8138db7d40f6333ff53a635927e10307fef222d8dbfd1126a2f9ba6e7cd04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112638"
---
# <a name="blocking-hook"></a>Enlace de bloqueo

Aunque este mecanismo es suficiente para aplicaciones sencillas, no puede admitir los complejos requisitos de distribución de mensajes de aplicaciones más avanzadas, como las que usan el modelo de interfaz de múltiples documentos (MDI). Para estas aplicaciones, la aplicación puede instalar un enlace de bloqueo específico del subproceso. El proveedor de servicios llamará a esto en lugar del enlace de bloqueo predeterminado descrito en el anterior. Un proveedor de servicios debe recuperar un puntero al enlace de bloqueo por subproceso de la32.dll Ws2 llamando a \_ [**WPUQueryBlockingCallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback). Si la aplicación no ha instalado su propio enlace de bloqueo, se devolverá un puntero a la función de enlace de bloqueo predeterminada.

Un proveedor de Windows sockets no puede asumir que un enlace de bloqueo proporcionado por la aplicación permite que el procesamiento de mensajes continúe como lo hace el enlace de bloqueo predeterminado. Algunas aplicaciones no pueden tolerar la posibilidad de volver a enviar mensajes mientras hay una operación de bloqueo pendiente. La función de enlace de bloqueo de una aplicación de este tipo simplemente devolvería **FALSE.** Si un proveedor de servicios depende de mensajes para su operación interna, puede ejecutar **PeekMessage**(hMyWnd...) antes de ejecutar el enlace de bloqueo de la aplicación para que pueda obtener sus propios mensajes sin afectar al resto del sistema.

No hay ningún enlace de bloqueo predeterminado instalado en versiones preferentes multiproceso de Windows. Esto se debe a que otros procesos no se bloquearán si una sola aplicación está esperando a que se complete una operación (y, por lo tanto, no llamar a **PeekMessage** o **GetMessage,** lo que hace que la aplicación desenrede el procesador en un estado Windows). Cuando el proveedor de servicios llama a [**WPUQueryBlockingCallback,**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback) se devolverá un puntero nulo que indica que el proveedor va a usar funciones de bloqueo del sistema operativo nativo. Sin embargo, para conservar la compatibilidad con versiones anteriores, todavía se puede instalar un enlace de bloqueo proporcionado por la aplicación por subproceso en Windows.

El proveedor de servicios Winsock llama al enlace de bloqueo solo si se cumplen todas las condiciones siguientes: la rutina es una que se define como capaz de bloquear, el socket especificado es un socket de bloqueo y la solicitud no se puede completar inmediatamente. Si solo se usan sockets que no son de bloqueo y [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) / [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) en lugar de [**WSPSelect,**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) nunca se llamará al enlace de bloqueo.

> [!Note]  
> Si, durante el tiempo que se usa el pseudobloqueo para bloquear un subproceso, se recibe un mensaje Windows para el subproceso, existe el riesgo de que el subproceso intente emitir otra llamada winsock. Debido a la dificultad de administrar esta condición de forma segura, la especificación Windows Sockets 1.1 no ha permitido este comportamiento. No está permitido que un subproceso determinado realice varias llamadas a funciones winsock anidadas. Solo se permite una llamada de función pendiente para un subproceso determinado. Las llamadas a funciones winsock anidadas producirán el error WSAEINPROGRESS. Debe destacarse que esta restricción se aplica tanto a las operaciones de bloqueo como a las de no bloqueo, pero solo en entornos Windows Sockets 1.1. Hay algunas excepciones a esta regla, incluidas dos funciones que permiten a una aplicación determinar si una operación de pseudobloqueo está en curso y cancelar dicha operación si es necesario. Estos se describen a continuación.

 

 

 
