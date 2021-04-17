---
description: Cualquier subproceso puede crear una ventana.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Crear ventanas en subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677863"
---
# <a name="creating-windows-in-threads"></a>Crear ventanas en subprocesos

Cualquier subproceso puede crear una ventana. El subproceso que crea la ventana es el propietario de la ventana y su cola de mensajes asociada. Por lo tanto, el subproceso debe proporcionar un bucle de mensajes para procesar los mensajes en su cola de mensajes. Además, debe usar [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) o [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) en ese subproceso, en lugar de las demás [funciones de espera](/windows/desktop/Sync/wait-functions), para que pueda procesar los mensajes. De lo contrario, se puede producir un interbloqueo del sistema cuando se envía un mensaje al subproceso mientras está esperando.

La función [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) se puede usar para permitir que un conjunto de subprocesos comparta el mismo estado de entrada. Al compartir el estado de entrada, los subprocesos comparten su concepto de la ventana activa. Al hacerlo, un subproceso siempre puede activar la ventana de otro subproceso. Esta función también es útil para compartir el estado del foco, el estado de la captura del mouse, el estado del teclado y el estado del orden Z de la ventana entre las ventanas creadas por subprocesos diferentes cuyo estado de entrada es compartido.

Para obtener información sobre cómo crear ventanas, vea [clases de Windows](../winmsg/window-classes.md).

 

 
