---
description: Sincronización de vmr con la frecuencia de actualización del monitor
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Sincronización de vmr con la frecuencia de actualización del monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4fa5055435d3adf737a3cdc253a3a43b041e5e849ac9c2b793ca37cedc78c0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072339"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a>Sincronización de vmr con la frecuencia de actualización del monitor

En escenarios poco frecuentes, es posible que desee sincronizar con precisión la representación de vídeo con la frecuencia de actualización del monitor, de modo que se presente exactamente un nuevo fotograma cada vez que se actualice el monitor. La manera más confiable de hacerlo es crear un asignador-presentador personalizado que use una operación de volteo en lugar de una operación blit para escribir los bits de vídeo en la superficie principal. Se llama a "Voltear" cada vez que se actualiza el monitor, por lo que si la secuencia de vídeo no contiene marcas de tiempo, el VMR se representará lo más rápido posible en la superficie principal, pero la superficie bloqueará la secuencia hasta que se complete la operación de volteo. Esto significa que, siempre que la CPU no se sobrecarga, el siguiente fotograma siempre estará esperando en la superficie principal cada vez que se actualice el monitor. Sin embargo, si se está ejecutando algún otro proceso con un uso intensivo de CPU, es posible que se desatenda el subproceso de streaming de DirectShow para que no pueda entregar fotogramas de vídeo lo suficientemente rápido como para la superficie principal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modo de reproducción sin representación de VMR (asignador-presentadores personalizados)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



