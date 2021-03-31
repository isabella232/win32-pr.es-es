---
description: Sincronizar la VMR con la frecuencia de actualización del monitor
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Sincronizar la VMR con la frecuencia de actualización del monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279016"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a>Sincronizar la VMR con la frecuencia de actualización del monitor

En raras ocasiones, es posible que desee sincronizar con precisión la representación de vídeo con la frecuencia de actualización del monitor, de modo que se presente exactamente un nuevo fotograma cada vez que se actualice el monitor. La forma más confiable de hacerlo es crear un asignador personalizado-presentador que use una operación de volteo en lugar de una operación de blit para escribir los bits de vídeo en la superficie principal. Se llama a "Flip" cada vez que se actualiza el monitor, por lo que si la secuencia de vídeo no contiene ninguna marca de tiempo, la VMR se representará lo más rápido posible a la superficie principal, pero la superficie bloqueará la secuencia hasta que se complete la operación de volteo. Esto significa que, siempre que no se sobrecargará la CPU, el siguiente fotograma siempre estará esperando en la superficie principal cada vez que se actualice el monitor. Sin embargo, si se está ejecutando algún otro proceso de uso intensivo de la CPU, podría privar el subproceso de streaming de DirectShow para que no pueda ofrecer fotogramas de vídeo lo suficientemente rápido a la superficie principal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modo de reproducción no representativo de VMR (asignador personalizado)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



