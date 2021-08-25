---
title: Escalar de volumen
description: Escalar de volumen
ms.assetid: a9fe2c35-9109-4697-9ffa-a31debbe72c8
keywords:
- Interfaz digital de instrumentar música (MIDI), escalar de volumen
- MIDI (Interfaz digital de instrumentador de música), escalar de volumen
- Asignador de MIDI, escalar de volumen
- escalar de volumen
- Asignador de MIDI, ajustar los niveles de salida
- ajustar los niveles de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7710e8e3ceb8079f04ac97bfcce8c91c6c74aa60452c220166e358a87939848
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804955"
---
# <a name="the-volume-scalar"></a>Escalar de volumen

El propósito del escalar de volumen es permitir ajustes entre los niveles de salida relativos de diferentes revisiones en un sintetizador. Por ejemplo, si la revisión de graves de un sintetizador es demasiado alta en comparación con su revisión de patch, puede cambiar el mapa de configuración para reducir verticalmente el volumen del bajo o el volumen del disco.

El escalar de volumen especifica un valor de porcentaje para cambiar todos los mensajes del controlador de volumen principal de MIDI que siguen a un mensaje de cambio de programa asociado. Por ejemplo, si el valor escalar del volumen es del 50 %, el asignador de MIDI modifica los mensajes del controlador de volumen principal de MIDI, como se muestra en la ilustración siguiente.

![imagen de mapeador de midi](images/mmap-a04.gif)

 

 




