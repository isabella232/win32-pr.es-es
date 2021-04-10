---
title: Iniciar, pausar y reanudar la reproducción
description: Iniciar, pausar y reanudar la reproducción
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- MCIWndPlay (macro)
- MCIWndPause (macro)
- MCIWndResume (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269403"
---
# <a name="starting-pausing-and-resuming-playback"></a>Iniciar, pausar y reanudar la reproducción

[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) es la macro de reproducción más general. Esta macro permite reproducir un archivo o un dispositivo desde la posición de reproducción actual. La reproducción continúa hasta el final del contenido a menos que se interrumpa.

Puede interrumpir temporalmente un dispositivo que se está reproduciendo con la macro [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) . Para reanudar la reproducción desde la posición en pausa, use la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) . Algunos dispositivos no admiten los comandos pausar y reanudar. Normalmente, estos dispositivos asignan **MCIWndPause** a la macro [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) , que detiene la reproducción o grabación. Puede reiniciar un dispositivo que no admita pausar o reanudar mediante **MCIWndPlay**, que inicia la reproducción desde la posición de reproducción actual.

 

 




