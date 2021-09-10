---
title: Tipos de eventos DE MIDI
description: Tipos de eventos DE MIDI
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- Interfaz digital de instrumentar música (MIDI), tipos de eventos
- MIDI (Interfaz digital de instrumentar música), tipos de eventos
- Estructura MIDIEVENT
- búferes de flujo, tipos de eventos DE MIDI
- Tipos de eventos DE MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370784"
---
# <a name="midi-event-types"></a>Tipos de eventos DE MIDI

El **miembro dwEvent** de la [**estructura MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) describe el evento MIDI que va a tener lugar. Los eventos cortos caben completamente en este miembro. Los eventos largos requieren uno o varios valores doubleword además del **miembro dwEvent** para almacenar las descripciones de eventos.

El byte alto del miembro **dwEvent** contiene información sobre si el evento es largo o corto y sobre si se genera una devolución de llamada junto con el evento . Además, este byte se usa para describir el tipo de evento. Los 24 bits restantes del miembro **dwEvent** se usan para contener los parámetros de evento (para mensajes cortos) o para contener la longitud de los parámetros de evento (para mensajes largos). Para extraer información del **miembro dwEvent,** use las macros [**\_ MEVT EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) y [**MEVT \_ EVENTPARM.**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)

Para obtener una descripción de los tipos de eventos predefinidos, vea el material de referencia de la **estructura MIDIEVENT.**

 

 