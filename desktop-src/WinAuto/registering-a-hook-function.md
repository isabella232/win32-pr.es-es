---
title: Registro de una función de enlace
description: Las aplicaciones cliente reciben WinEvents en una función de devolución de llamada WinEventProc. La aplicación define las acciones realizadas por la función de devolución de llamada, pero la sintaxis debe ser como se especifica en el prototipo.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c444d2ee291cb07386e775a649ba0c3d42486c45b70e4d3f4629b9b67274f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564655"
---
# <a name="registering-a-hook-function"></a>Registro de una función de enlace

Las aplicaciones cliente reciben WinEvents en una función de devolución de [*llamada WinEventProc.*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) La aplicación define las acciones realizadas por la función de devolución de llamada, pero la sintaxis debe ser como se especifica en el prototipo.

Para poder recibir eventos, la función debe registrarse mediante una llamada a [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook). El cliente puede llamar a **SetWinEventHook** más de una vez para registrar diferentes funciones de enlace o para establecer eventos adicionales para una función de enlace registrada previamente.

Al llamar [**a SetWinEventHook,**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) el cliente especifica qué eventos recibir y cómo recibirlos. El cliente puede elegir:

-   Recibir todos los eventos o un conjunto específico de eventos.
-   Recibir eventos de todos los subprocesos o de un subproceso específico.
-   Recibir eventos de todos los procesos o de un proceso específico.
-   Controlar eventos en proceso o fuera de proceso.

Cuando se genera un evento que coincide con los criterios especificados, el sistema llama a la función de devolución de llamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) del cliente (o "procedimiento de enlace"). Los parámetros que recibe la función de enlace le informen al cliente sobre la ventana, el objeto y el posible elemento secundario que generó el evento. Un cliente usa estos parámetros en una llamada de recuperación de objetos, como [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

 




