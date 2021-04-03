---
title: Codificación de Two-Pass
description: Codificación de Two-Pass
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media Format SDK, codificación de dos pasos
- Windows Media Format SDK, codificación de paso 2
- códecs, codificación de dos pasos
- códecs, codificación de 2 pasos
- codificación de dos pasos, acerca de
- 2-paso de codificación, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6764f80857447e122c97c69683243a65da7e83b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075482"
---
# <a name="two-pass-encoding"></a>Codificación de Two-Pass

La codificación de dos pasos es un método de codificación disponible con algunos códecs, como el códec Windows Media Video 9. Cuando se usa la codificación de dos pasos, el códec procesa dos veces todos los ejemplos de la secuencia. En el primer paso, el códec recopila información sobre el contenido de la secuencia. En el segundo paso, el códec usa la información recopilada en el primer paso para optimizar el proceso de codificación de la secuencia.

En el modo de codificación de velocidad de bits constante, los archivos codificados en dos fases suelen ser más eficaces que los archivos codificados en un solo paso. La VBR basada en la calidad, que es una pasada, genera una calidad más coherente que la VBR basada en la velocidad de bits, que es de dos pasos.

No se puede usar la codificación de dos pasos en secuencias en directo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del códec**](codec-features.md)
</dt> <dt>

[**Uso de la codificación de Two-Pass**](using-two-pass-encoding.md)
</dt> </dl>

 

 




