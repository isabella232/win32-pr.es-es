---
title: Invertir reproducción
description: Invertir reproducción
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- MCIWndPlayReverse (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418667"
---
# <a name="reversing-playback"></a>Invertir reproducción

Algunos dispositivos admiten la reproducción en dirección inversa. Puede reproducir el contenido de este dispositivo en la dirección inversa mediante la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) . Esta macro define el ámbito de reproducción desde la posición de reproducción actual hasta el principio del contenido. El dispositivo de vídeo digital, MCIAVI. DRV, puede reproducirse hacia atrás. Los dispositivos que no pueden reproducirse hacia atrás, como el audio de CD, pueden emitir un mensaje de error cuando se invoca **MCIWndPlayReverse** .

 

 




