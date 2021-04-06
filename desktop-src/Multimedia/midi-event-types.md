---
title: Tipos de eventos MIDI
description: Tipos de eventos MIDI
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- Interfaz digital de instrumentos musicales (MIDI), tipos de evento
- MIDI (interfaz digital de instrumentos musicales), tipos de evento
- Estructura MIDIEVENT
- búferes de secuencia, tipos de eventos MIDI
- Tipos de eventos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077731"
---
# <a name="midi-event-types"></a>Tipos de eventos MIDI

El miembro **dwEvent** de la estructura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) describe el evento MIDI que debe tener lugar. Los eventos cortos solo se ajustan a este miembro. Los eventos Long requieren uno o varios valores de palabra además del miembro **dwEvent** para almacenar las descripciones de evento.

El byte alto del miembro **dwEvent** contiene información sobre si el evento es largo o corto y sobre si se genera una devolución de llamada junto con el evento. Además, este byte se utiliza para describir el tipo de evento. Los 24 bits restantes del miembro **dwEvent** se usan para contener los parámetros de evento (para mensajes cortos) o para contener la longitud de los parámetros de evento (para los mensajes largos). Para extraer información del miembro **dwEvent** , use las macros [**MEVT \_ EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) y [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) .

Para obtener una descripción de los tipos de eventos predefinidos, consulte el material de referencia de la estructura **MIDIEVENT** .

 

 