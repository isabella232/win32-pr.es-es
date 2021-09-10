---
title: Clave Mapas
description: Clave Mapas
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- Interfaz digital de instrumentador de música (MIDI),Asignador de MIDI
- MIDI (Interfaz digital instrumenta instrumenta),Asignador DE MIDI
- Asignador de MIDI, mapas de claves
- mapas de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffafd99e6d813f12c388b633997980b7a58d62dc
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371054"
---
# <a name="key-maps"></a>Clave Mapas

Cada entrada de la tabla de traducción del mapa de revisiones puede tener un mapa de claves asociado. Los mapas de claves afectan a los mensajes note-on, note-off y polyfónic-key-aftertouch. Un mapa de claves tiene una tabla de traducción con una entrada para cada uno de los 128 valores de clave MIDI. Por ejemplo, si la entrada del valor de clave 60 es 72, el asignador de MIDI modifica los mensajes de nota de MIDI como se muestra en la ilustración siguiente.

![imagen del asignador de midi](images/mmap-a06.gif)

Los mapas de claves son útiles con los sintetizadores que tienen instrumentales de sonido basados en claves con un sonido de sonido especial asignado a cada clave. Normalmente, los mapas clave se asignan a la primera revisión de los mapas de revisión en los canales de la zona (10 y 16).

 

 




