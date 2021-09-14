---
title: Codificación de velocidad de bits constante (CBR)
description: Codificación de velocidad de bits constante (CBR)
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- Windows SDK de formato multimedia, codificación CBR
- Windows SDK de formato multimedia, velocidad de bits constante (CBR)
- códecs, codificación CBR
- codecs,constant bit rate (CBR)
- velocidad de bits constante (CBR)
- CBR (velocidad de bits constante)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251499"
---
# <a name="constant-bit-rate-cbr-encoding"></a>Codificación de velocidad de bits constante (CBR)

La codificación de velocidad de bits constante (CBR) es el método predeterminado de codificación con Windows SDK de formato multimedia. Cuando se usa la codificación CBR, se especifica la velocidad de bits de destino para una secuencia y el códec usa la cantidad de compresión necesaria para lograrlo.

Con la codificación CBR, la velocidad de bits y el tamaño de la secuencia codificada se conocen antes de la codificación. Por ejemplo, si codifica una canción de tres minutos a 32 000 bits por segundo, sabe que el tamaño del archivo será de aproximadamente 704 kilobytes (32 000 bps x 180 segundos/8 bits por byte/1024). También sabe que el ancho de banda necesario para transmitir el contenido codificado es de aproximadamente 32 000 bits por segundo.

La codificación de velocidad de bits variable restringida (descrita en la sección siguiente) también le permite conocer la velocidad de bits antes de la codificación, pero como la velocidad es variable, el archivo resultante no se puede transmitir de forma tan eficaz como un archivo codificado en modo CBR. Con CBR, la velocidad de bits con el tiempo siempre permanece cerca de la velocidad de bits promedio o objetivo, y se puede especificar la cantidad de variación.

La desventaja de la codificación CBR es que la calidad del contenido codificado no será constante. Dado que algunos contenidos son más difíciles de comprimir, las partes de una secuencia CBR serán de menor calidad que otras. Por ejemplo, una película típica tiene algunas escenas bastante estáticas y otras que están llenas de acción. Si codifica una película mediante CBR, las escenas estáticas y, por tanto, fáciles de codificar de forma eficaz, serán de mayor calidad que las escenas de acción, que son mucho más difíciles de codificar de forma eficaz.

La codificación CBR también puede dar lugar a una calidad incoherente de un archivo a otro. Si usa CBR para codificar varias canciones de distintos géneros a la misma velocidad de bits, es posible que observe alguna diferencia de calidad entre ellas.

En general, las variaciones en la calidad de un archivo CBR se pronuncian más a velocidades de bits más bajas. A velocidades de bits más altas, la calidad de un archivo codificado con CBR seguirá variando, pero los problemas de calidad serán menos perceptibles para el usuario. Al usar la codificación CBR, debe establecer el ancho de banda tan alto como lo permita el escenario de entrega.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elegir un método de codificación**](choosing-an-encoding-method.md)
</dt> <dt>

[**Características del códec**](codec-features.md)
</dt> <dt>

[**Codificación de velocidad de bits variable (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




