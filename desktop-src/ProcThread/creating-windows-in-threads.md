---
description: Cualquier subproceso puede crear una ventana.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Crear Windows en subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2084536ff43ea4c52efb179177fe6f6c803c49b9f580b2d298b73e9b528f1a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143098"
---
# <a name="creating-windows-in-threads"></a>Crear Windows en subprocesos

Cualquier subproceso puede crear una ventana. El subproceso que crea la ventana posee la ventana y su cola de mensajes asociada. Por lo tanto, el subproceso debe proporcionar un bucle de mensajes para procesar los mensajes de su cola de mensajes. Además, debe usar [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) o [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) en ese subproceso, en lugar de las otras funciones [de](/windows/desktop/Sync/wait-functions)espera , para que pueda procesar mensajes. De lo contrario, el sistema puede quedar interbloqueado cuando se envía un mensaje al subproceso mientras está esperando.

La [**función AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) se puede usar para permitir que un conjunto de subprocesos comparta el mismo estado de entrada. Al compartir el estado de entrada, los subprocesos comparten su concepto de la ventana activa. Al hacerlo, un subproceso siempre puede activar la ventana de otro subproceso. Esta función también es útil para compartir el estado de foco, el estado de captura del mouse, el estado del teclado y el estado del orden Z de la ventana entre ventanas creadas por subprocesos diferentes cuyo estado de entrada se comparte.

Para obtener información sobre cómo crear ventanas, [vea Windows clases](../winmsg/window-classes.md).

 

 
