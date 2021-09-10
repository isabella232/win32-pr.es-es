---
title: Detener, pausar y reanudar un dispositivo
description: Detener, pausar y reanudar un dispositivo
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- MCI_STOP comando
- MCI_PAUSE comando
- MCI_RESUME comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddcd9618608226dec108d62754964fe6401d429
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371696"
---
# <a name="stopping-pausing-and-resuming-a-device"></a>Detener, pausar y reanudar un dispositivo

El [**comando stop**](stop.md) [**(MCI \_ STOP)**](mci-stop.md)suspende la reproducción o grabación de un dispositivo. Muchos dispositivos también admiten [**el comando pause**](pause.md) ([**MCI \_ PAUSE**](mci-pause.md)). La diferencia entre **detener** y **pausar** depende del dispositivo. Normalmente, **pausa** la operación, pero deja el dispositivo listo para reanudar la reproducción o la grabación inmediatamente.

El uso del comando [**play**](play.md) ([**MCI \_ PLAY**](mci-play.md)) o [**record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) para reiniciar un dispositivo restablece las ubicaciones especificadas con las marcas "to" (MCI TO) y "from" (MCI FROM) antes de que el dispositivo se pausase o se \_ \_ detuve. Sin la marca "from", estos comandos restablecen la ubicación inicial a la posición actual. Sin la marca "to", restablecen la ubicación final al final del medio. Para continuar reproduciendo o grabando sin restablecer una  posición de detenerse especificada previamente, use la marca "to" del comando play o **record** para especificar una posición final.

Algunos dispositivos admiten [**el comando resume**](resume.md) [**(MCI \_ RESUME)**](mci-resume.md)para reiniciar un dispositivo en pausa. Este comando no cambia las ubicaciones "to" y "from" especificadas con el comando **play** o **record** que precedía al [**comando pause.**](pause.md)

 

 




