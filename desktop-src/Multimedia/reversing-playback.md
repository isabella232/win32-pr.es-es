---
title: Invertir la reproducción
description: Invertir la reproducción
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- Macro MCIWndPlayReverse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372445"
---
# <a name="reversing-playback"></a>Invertir la reproducción

Algunos dispositivos admiten la reproducción en la dirección inversa. Puede reproducir el contenido de este tipo de dispositivo en la dirección inversa mediante la macro [**MCIWndPlayReverse.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) Esta macro define el ámbito de reproducción desde la posición de reproducción actual hasta el principio del contenido. El dispositivo de vídeo digital, MCIAVI. DRV, puede reproducirse hacia atrás. Los dispositivos que no se pueden reproducir con versiones anteriores, como el audio de CD, pueden emitir un mensaje de error cuando se invoca **MCIWndPlayReverse.**

 

 




