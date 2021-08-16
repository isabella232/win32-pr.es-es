---
description: Pseudobloqueo de operaciones de pseudobloqueo en Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudobloqueo y bloqueo verdadero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371935a2f8984ebd080da48492807b3f5ffa9286b991b16b516244ccf26ee093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740947"
---
# <a name="pseudo-blocking-and-true-blocking"></a>Pseudobloqueo y bloqueo verdadero

En 16 Windows entornos, el sistema operativo no admite el bloqueo verdadero. Por lo tanto, una operación de bloqueo que no se puede completar inmediatamente se controla de la siguiente manera:

-   El proveedor de servicios inicia la operación y, a continuación, entra en un bucle durante el cual envía los mensajes Windows (lo que produce el procesador a otro subproceso si es necesario).
-   A continuación, comprueba la finalización de la Windows Sockets.
-   Si se ha completado la función o si se ha invocado [**WSPCancelBlockingCall,**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) el bucle finaliza y la función de bloqueo se completa con un resultado adecuado.

Esto es lo que significa el término pseudobloqueo y el bucle al que se hace referencia anteriormente se conoce como el enlace de bloqueo predeterminado.

 

 
