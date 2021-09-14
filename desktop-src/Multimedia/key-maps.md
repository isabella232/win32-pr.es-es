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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246189"
---
# <a name="key-maps"></a>Clave Mapas

Cada entrada de la tabla de traducción del mapa de revisiones puede tener un mapa de claves asociado. Los mapas de claves afectan a los mensajes note-on, note-off y polyfónic-key-aftertouch. Un mapa de claves tiene una tabla de traducción con una entrada para cada uno de los 128 valores de clave MIDI. Por ejemplo, si la entrada del valor de clave 60 es 72, el asignador de MIDI modifica los mensajes de nota de MIDI como se muestra en la ilustración siguiente.

![imagen del asignador de midi](images/mmap-a06.gif)

Los mapas de claves son útiles con los sintetizadores que tienen instrumentales de sonido basados en claves con un sonido de sonido especial asignado a cada clave. Normalmente, los mapas clave se asignan a la primera revisión de los mapas de revisión en los canales de la zona (10 y 16).

 

 




