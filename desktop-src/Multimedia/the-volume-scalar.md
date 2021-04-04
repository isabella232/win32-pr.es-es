---
title: El volumen escalar
description: El volumen escalar
ms.assetid: a9fe2c35-9109-4697-9ffa-a31debbe72c8
keywords:
- Interfaz digital de instrumentos musicales (MIDI), volumen escalar
- MIDI (interfaz digital de instrumentos musicales), escalar volumen
- Asignador de MIDI, escalar de volumen
- escalar del volumen
- Asignador de MIDI, ajustar los niveles de salida
- ajustar los niveles de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39566a10ca909030b60ff197f009b6afe05ce51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076381"
---
# <a name="the-volume-scalar"></a>El volumen escalar

El propósito del volumen escalar es permitir ajustes entre los niveles de salida relativos de distintas revisiones en un sintetizador. Por ejemplo, si la revisión de graves de un sintetizador es demasiado alta en comparación con su revisión de piano, puede cambiar el mapa de configuración para reducir el volumen de graves o el volumen de piano hacia arriba.

El volumen escalar especifica un valor de porcentaje para cambiar todos los mensajes de controlador principal de volumen MIDI que siguen un mensaje de cambio de programa asociado. Por ejemplo, si el valor escalar del volumen es del 50%, el asignador MIDI modifica los mensajes del controlador principal del volumen MIDI, tal como se muestra en la siguiente ilustración.

![imagen del asignador MIDI](images/mmap-a04.gif)

 

 




