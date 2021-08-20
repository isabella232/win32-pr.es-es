---
title: Clave Mapas
description: Clave Mapas
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- Interfaz digital de instrumentador de música (MIDI),Asignador de MIDI
- MIDI (Interfaz digital de instrumentador de música),Asignador DE MES
- Asignador de MIDI, mapas clave
- mapas de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72197de28a6596efa951b302f0ca351ac187532cd28d431cf1d954b53d841064
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140233"
---
# <a name="key-maps"></a>Clave Mapas

Cada entrada de la tabla de traducción del mapa de revisiones puede tener un mapa de claves asociado. Los mapas de claves afectan a los mensajes note-on, note-off y polyphonic-key-aftertouch. Un mapa de claves tiene una tabla de traducción con una entrada para cada uno de los 128 valores de clave MIDI. Por ejemplo, si la entrada para el valor de clave 60 es 72, el asignador de MIDI modifica los mensajes de nota-on de MIDI como se muestra en la ilustración siguiente.

![imagen de mapeador de midi](images/mmap-a06.gif)

Los mapas de claves son útiles con los sintetizadores que tienen instrumentoes de sonido basados en claves con un sonido de sonido de sonido particular asignado a cada clave. Normalmente, los mapas de claves se asignan a la primera revisión de los mapas de revisión en los canales de tratamiento (10 y 16).

 

 




