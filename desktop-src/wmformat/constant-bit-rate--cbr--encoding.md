---
title: Codificación de velocidad de bits constante (CBR)
description: Codificación de velocidad de bits constante (CBR)
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- Windows Media Format SDK, codificación CBR
- Windows Media Format SDK, velocidad de bits constante (CBR)
- códecs, codificación CBR
- códecs, velocidad de bits constante (CBR)
- velocidad de bits constante (CBR)
- CBR (velocidad de bits constante)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419051"
---
# <a name="constant-bit-rate-cbr-encoding"></a>Codificación de velocidad de bits constante (CBR)

La codificación de velocidad de bits constante (CBR) es el método predeterminado de codificación con el SDK de Windows Media Format. Cuando se usa la codificación CBR, se especifica la velocidad de bits de destino de una secuencia y el códec utiliza cualquier cantidad de compresión necesaria para lograrlo.

Con la codificación CBR, la velocidad de bits y el tamaño de la secuencia codificada se conocen antes de la codificación. Por ejemplo, si está codificando una canción de tres minutos en 32.000 bits por segundo, sabe que el tamaño del archivo será de aproximadamente 704 kilobytes (32.000 BPS x 180 segundos/8 bits por byte/1.024). También sabe que el ancho de banda necesario para transmitir por secuencias el contenido codificado es aproximadamente 32.000 bits por segundo.

La codificación de velocidad de bits variable restringida (descrita en la sección siguiente) también le permite conocer la velocidad de bits antes de la codificación, pero como la velocidad es variable, el archivo resultante no se puede transmitir de forma eficaz como un archivo codificado en modo CBR. Con CBR, la velocidad de bits a lo largo del tiempo siempre permanece cerca de la velocidad de bits media o de destino, y se puede especificar la cantidad de variación.

La desventaja de la codificación CBR es que la calidad del contenido codificado no será constante. Dado que el contenido es más difícil de comprimir, las partes de un flujo CBR serán de menor calidad que otras. Por ejemplo, una película típica tiene algunas escenas que son bastante estáticas y algunas escenas que están llenas de acción. Si codifica una película con CBR, las escenas que son estáticas y, por lo tanto, resultan fáciles de codificar de forma eficaz, tendrán una mayor calidad que las escenas de acción, que son mucho más difíciles de codificar de forma eficaz.

La codificación CBR también puede producir una calidad incoherente de un archivo a otro. Si usa CBR para codificar varias canciones de géneros diferentes a la misma velocidad de bits, puede observar una diferencia en la calidad entre ellos.

En general, las variaciones en la calidad de un archivo CBR son más pronunciadas a velocidades de bits inferiores. A velocidades de bits más altas, la calidad de un archivo con codificación CBR seguirá variando, pero los problemas de calidad serán menos perceptibles para el usuario. Cuando se usa la codificación CBR, se debe establecer el ancho de banda tan alto como permita el escenario de entrega.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elección de un método de codificación**](choosing-an-encoding-method.md)
</dt> <dt>

[**Características del códec**](codec-features.md)
</dt> <dt>

[**Codificación de velocidad de bits variable (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




