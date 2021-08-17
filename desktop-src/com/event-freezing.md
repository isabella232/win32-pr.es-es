---
title: Inmovilización de eventos
description: Inmovilización de eventos
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba439ebce12a48d78e1eb1d2daa31990c02f4a42082d3425e9b6ef2f842b3ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736805"
---
# <a name="event-freezing"></a>Inmovilización de eventos

Un contenedor puede notificar a un control que no está listo para responder a eventos llamando a [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **TRUE.** Puede descongelar los eventos llamando a **FreezeEvents** con **FALSE.** Cuando un contenedor inmoviliza eventos, se inmoviliza el procesamiento de eventos, no la recepción de eventos. es decir, un contenedor todavía puede recibir eventos mientras los eventos están inmovilizados. Si un contenedor recibe una notificación de eventos mientras sus eventos están inmovilizados, el contenedor debe omitir el evento. Ninguna otra acción es adecuada.

Un control debe tomar nota de la llamada de un contenedor a [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **TRUE** si es importante para el control que un evento no se pierde. Mientras se inmoviliza el procesamiento de eventos de un contenedor, un control debe implementar una de las técnicas siguientes:

-   Desen marcha los eventos con el conocimiento completo de que el contenedor no realizará ninguna acción.
-   Descarte todos los eventos que el control habría desencadenado.
-   Poner en cola todos los eventos pendientes y desenvirlos después de que el contenedor haya llamado a [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **FALSE.**
-   Poner en cola solo eventos importantes o relevantes y desen marcharlos después de que el contenedor haya llamado [**a FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) con **FALSE.**

Cada técnica es aceptable y adecuada en diferentes circunstancias. El desarrollador del control es responsable de determinar e implementar la técnica adecuada para la funcionalidad del control.

 

 




