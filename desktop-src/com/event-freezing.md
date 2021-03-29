---
title: Congelación de eventos
description: Congelación de eventos
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e403448d53949c263b8e146961690de1200436c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903424"
---
# <a name="event-freezing"></a>Congelación de eventos

Un contenedor puede notificar a un control que no está listo para responder a eventos mediante una llamada a [**IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **true**. Puede liberar los eventos llamando a **FreezeEvents** con **false**. Cuando un contenedor inmoviliza eventos, está inmovilizando el procesamiento de eventos, no la recepción de eventos; es decir, un contenedor todavía puede recibir eventos mientras los eventos se inmovilizan. Si un contenedor recibe una notificación de eventos mientras sus eventos están inmovilizados, el contenedor debe omitir el evento. No es adecuado ninguna otra acción.

Un control debe tomar nota de la llamada de un contenedor a [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **true** si es importante para el control que no se ha perdido un evento. Mientras el procesamiento de eventos de un contenedor está inmovilizado, un control debe implementar una de las técnicas siguientes:

-   Active los eventos en el conocimiento completo de que el contenedor no realizará ninguna acción.
-   Descartar todos los eventos que el control habría desencadenado.
-   Poner en cola todos los eventos pendientes y activarlos después de que el contenedor haya llamado a [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **false**.
-   Poner en cola solo eventos relevantes o importantes y activarlos después de que el contenedor haya llamado a [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **false**.

Cada técnica es aceptable y adecuada en diferentes circunstancias. El desarrollador del control es responsable de determinar e implementar la técnica adecuada para la funcionalidad del control.

 

 




