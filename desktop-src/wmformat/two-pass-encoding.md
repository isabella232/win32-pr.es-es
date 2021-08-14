---
title: Two-Pass codificación
description: Two-Pass codificación
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows SDK de formato multimedia, codificación de dos pases
- Windows SDK de formato multimedia, codificación de 2 pases
- códecs, codificación de dos pases
- códecs, codificación de 2 pases
- codificación de dos pases, acerca de
- Codificación de 2 pases, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cd769049b5fa3869c844e00d9ee14cfae596b197d06d414b04a544d831bbeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845343"
---
# <a name="two-pass-encoding"></a>Two-Pass codificación

La codificación de dos pases es un método de codificación disponible con algunos códecs, como el códec Windows Media Video 9. Cuando se usa la codificación de dos pases, el códec procesa todas las muestras de la secuencia dos veces. En el primer paso, el códec recopila información sobre el contenido de la secuencia. En el segundo paso, el códec usa la información recopilada en el primer paso para optimizar el proceso de codificación de la secuencia.

En el modo de codificación Velocidad de bits constante, los archivos codificados en dos pases suelen ser más eficaces que los archivos codificados en un solo paso. El VBR basado en calidad, que es un paso, genera una calidad más coherente que la VBR basada en velocidad de bits, que es de dos pases.

No se puede usar la codificación de dos pases en secuencias en vivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del códec**](codec-features.md)
</dt> <dt>

[**Uso de Two-Pass codificación**](using-two-pass-encoding.md)
</dt> </dl>

 

 




