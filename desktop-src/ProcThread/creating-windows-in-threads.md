---
description: Cualquier subproceso puede crear una ventana.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Creación de Windows en subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073886"
---
# <a name="creating-windows-in-threads"></a>Creación de Windows en subprocesos

Cualquier subproceso puede crear una ventana. El subproceso que crea la ventana posee la ventana y su cola de mensajes asociada. Por lo tanto, el subproceso debe proporcionar un bucle de mensajes para procesar los mensajes de su cola de mensajes. Además, debe usar [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) o [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) en ese subproceso, en lugar de las demás funciones de espera [,](/windows/desktop/Sync/wait-functions)para que pueda procesar mensajes. De lo contrario, el sistema puede quedar interbloqueado cuando se envía un mensaje al subproceso mientras está en espera.

La [**función AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) se puede usar para permitir que un conjunto de subprocesos comparta el mismo estado de entrada. Al compartir el estado de entrada, los subprocesos comparten su concepto de la ventana activa. Al hacerlo, un subproceso siempre puede activar la ventana de otro subproceso. Esta función también es útil para compartir el estado de enfoque, el estado de captura del mouse, el estado del teclado y el estado del orden Z de la ventana entre ventanas creadas por subprocesos diferentes cuyo estado de entrada se comparte.

Para obtener información sobre cómo crear ventanas, [vea Windows clases](../winmsg/window-classes.md).

 

 
