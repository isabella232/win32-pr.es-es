---
title: Registro de una función de enlace
description: Las aplicaciones cliente reciben WinEvents en una función de devolución de llamada WinEventProc. La aplicación define las acciones realizadas por la función de devolución de llamada, pero la sintaxis debe ser como se especifica en el prototipo.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b1f39a535b366af72b1034cc9344171d253ea0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903291"
---
# <a name="registering-a-hook-function"></a>Registro de una función de enlace

Las aplicaciones cliente reciben WinEvents en una función de devolución de llamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) . La aplicación define las acciones realizadas por la función de devolución de llamada, pero la sintaxis debe ser como se especifica en el prototipo.

Antes de poder recibir eventos, la función se debe registrar llamando a [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook). El cliente puede llamar a **SetWinEventHook** más de una vez para registrar distintas funciones de enlace o para establecer eventos adicionales para una función de enlace registrada previamente.

Al llamar a [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) , el cliente especifica qué eventos se van a recibir y cómo recibirlos. El cliente puede elegir:

-   Recibir todos los eventos o un conjunto específico de eventos.
-   Recibir eventos de todos los subprocesos o de un subproceso específico.
-   Recibir eventos de todos los procesos o de un proceso específico.
-   Controlar eventos en proceso o fuera de proceso.

Cuando se genera un evento que coincide con los criterios especificados, el sistema llama a la función de devolución de llamada de [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) del cliente (o al "procedimiento de enlace"). Los parámetros que recibe la función de enlace indican al cliente sobre la ventana, el objeto y el posible elemento secundario que generó el evento. Un cliente usa estos parámetros en una llamada de recuperación de objeto, como [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

 




