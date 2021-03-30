---
title: Detener, pausar y reanudar un dispositivo
description: Detener, pausar y reanudar un dispositivo
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- Comando MCI_STOP
- Comando MCI_PAUSE
- Comando MCI_RESUME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddcd9618608226dec108d62754964fe6401d429
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776237"
---
# <a name="stopping-pausing-and-resuming-a-device"></a>Detener, pausar y reanudar un dispositivo

El comando [**detener**](stop.md) ([**MCI \_ Stop**](mci-stop.md)) suspende la reproducción o grabación de un dispositivo. Muchos dispositivos también admiten el comando [**pausar**](pause.md) ([**MCI \_ PAUSE**](mci-pause.md)). La diferencia entre **detener** y **pausar** depende del dispositivo. Normalmente **pausa** suspende la operación, pero deja el dispositivo listo para reanudar la reproducción o grabación inmediatamente.

Con el comando [**reproducir**](play.md) ([**MCI \_ Play**](mci-play.md)) o [**registro**](record.md) ([**\_ registro de MCI**](mci-record.md)) para reiniciar un dispositivo, se restablecen las ubicaciones especificadas con las marcas "to" (MCI \_ to) y "from" (MCI \_ from) antes de que el dispositivo se haya pausado o detenido. Sin la marca "desde", estos comandos restablecen la ubicación inicial a la posición actual. Sin la marca "para", restablecen la ubicación final al final del medio. Para seguir reproduciendo o grabando sin restablecer una posición de detención especificada previamente, use la marca "para" del comando **Play** o **Record** para especificar una posición final.

Algunos dispositivos admiten el comando [**reanudar**](resume.md) ([**\_ reanudar MCI**](mci-resume.md)) para reiniciar un dispositivo en pausa. Este comando no cambia las ubicaciones "to" y "from" especificadas con el comando **Play** o **Record** que precedía al comando [**PAUSE**](pause.md) .

 

 




