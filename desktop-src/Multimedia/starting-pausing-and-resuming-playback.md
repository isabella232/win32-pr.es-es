---
title: Inicio, pausa y reanudación de la reproducción
description: Inicio, pausa y reanudación de la reproducción
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- Macro MCIWndPlay
- Macro MCIWndPause
- Macro MCIWndResume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372439"
---
# <a name="starting-pausing-and-resuming-playback"></a>Inicio, pausa y reanudación de la reproducción

[**MCIWndPlay es**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) la macro de reproducción más general. Esta macro le permite reproducir un archivo o dispositivo desde la posición de reproducción actual. La reproducción continúa hasta el final del contenido a menos que se interrumpa.

Puede interrumpir temporalmente un dispositivo que se está reproduciendo mediante la macro [**MCIWndPause.**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) Para reanudar la reproducción desde la posición en pausa, use la macro [**MCIWndResume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) Algunos dispositivos no admiten los comandos de pausa y reanudación. Estos dispositivos suelen asignar **MCIWndPause** a la macro [**MCIWndStop,**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) que detiene la reproducción o grabación. Puede reiniciar un dispositivo que no admita pausas o reanudaciones mediante **MCIWndPlay,** que inicia la reproducción desde la posición de reproducción actual.

 

 




