---
description: Pseudoblocking las operaciones de pseudo bloqueo en Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo bloqueo y bloqueo real
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696810"
---
# <a name="pseudo-blocking-and-true-blocking"></a>Pseudo bloqueo y bloqueo real

En 16 entornos Windows, el sistema operativo no admite el bloqueo verdadero; por lo tanto, una operación de bloqueo que no se puede completar inmediatamente se administra de la siguiente manera:

-   El proveedor de servicios inicia la operación y, a continuación, entra en un bucle durante el que envía los mensajes de Windows (lo que produce el procesador a otro subproceso si es necesario).
-   A continuación, comprueba la finalización de la función de Windows Sockets.
-   Si la función se ha completado, o si se ha invocado [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) , el bucle se termina y la función de bloqueo se completa con un resultado adecuado.

Esto es lo que se debe a la condición de pseudo bloqueo y el bucle al que se hace referencia anteriormente se conoce como el enlace de bloqueo predeterminado.

 

 
