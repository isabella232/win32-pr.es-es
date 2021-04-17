---
title: Low-Delay audio
description: Low-Delay audio
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- Windows Media Format SDK, audio con retraso bajo
- SDK de Windows Media Format, compatibilidad de audio
- códecs, audio con retraso bajo
- códecs, compatibilidad de audio
- audio con retraso bajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695464"
---
# <a name="low-delay-audio"></a>Low-Delay audio

El audio de retraso bajo es un modo de codificación que genera audio comprimido con una configuración de ventana de búfer más pequeña que otros modos. Esto resulta útil para las secuencias que se deben cambiar rápidamente durante la reproducción. El escenario típico de esta característica es una presentación en streaming que incluye la capacidad de cambiar el contenido de forma arbitraria, como cambiar el canal de un televisor.

Cuando se usa un formato de audio de retraso bajo, la latencia para cambiar el contenido se reduce drásticamente en comparación con otros formatos de audio. También se reduce la latencia para las difusiones en vivo cuando se usan formatos de retraso bajo.

Esta característica es compatible con los códecs Windows Media Audio 9,1 y Windows Media Audio 9,1 Professional. Los formatos de retraso bajo solo están disponibles para la codificación de velocidad de bits constante (tanto un paso como dos pasos).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del códec**](codec-features.md)
</dt> </dl>

 

 




