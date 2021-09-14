---
title: Low-Delay Audio
description: Low-Delay Audio
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- Windows SDK de formato multimedia, audio de retraso bajo
- Windows SDK de formato multimedia, compatibilidad con audio
- códecs, audio de bajo retraso
- códecs, compatibilidad con audio
- audio con retraso bajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267047"
---
# <a name="low-delay-audio"></a>Low-Delay Audio

El audio de bajo retraso es un modo de codificación que genera audio comprimido con una configuración de ventana de búfer más pequeña que otros modos. Esto es útil para las secuencias que deben cambiarse rápidamente durante la reproducción. El escenario típico de esta característica es una presentación en streaming que incluye la capacidad de cambiar contenido arbitrariamente, como cambiar el canal de una televisión.

Cuando se usa un formato de audio de bajo retraso, la latencia para cambiar el contenido se reduce drásticamente en comparación con otros formatos de audio. La latencia también se reduce para las retransmisiones en directo cuando se usan formatos de retraso bajo.

Esta característica es compatible con los códecs Windows Media Audio 9.1 y Windows Media Audio 9. Professional 1. Los formatos de retraso bajo solo están disponibles para la codificación de velocidad de bits constante (un paso y dos pases).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del códec**](codec-features.md)
</dt> </dl>

 

 




