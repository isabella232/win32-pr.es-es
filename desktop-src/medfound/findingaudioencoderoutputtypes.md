---
description: Búsqueda de tipos de salida del codificador de audio
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Buscar tipos de salida del codificador de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5389274cca1178ebc0ae03e21f7a804f73a5db48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465918"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a>Buscar tipos de salida del codificador de audio (Microsoft Media Foundation)

Dado que debe usar un formato de salida de codificador de audio enumerado por el codificador de audio, debe tener una manera de encontrar el formato más adecuado para sus necesidades. El número de canales, bits por muestra y frecuencia de muestreo de la salida que elija debe coincidir con los valores del contenido que comprima. Sin embargo, el codificador puede admitir varios tipos dentro de estas restricciones.

El factor determinante para elegir un tipo es la velocidad de bits de la secuencia codificada. quiere encontrar un tipo de medio que coincida con la entrada y que tenga una velocidad de bits lo más cercana posible a un valor de destino. Si va a enumerar los tipos de salida de VBR de un solo paso, es el valor de calidad el que decide el tipo que usa. Para obtener más información sobre los valores de calidad en los tipos de salida enumerados, vea [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).

> [!Note]  
>    El codificador de audio enumera algunos tipos que son duplicados de otros tipos de casi todas las maneras. Estos duplicados existen para formatos en los que el número de paquetes por segundo no cumple los requisitos de almacenamiento en archivos ASF cuando se sincronizan con vídeo. El audio sincronizado con vídeo en un archivo ASF debe tener 3 o más paquetes por segundo para velocidades de bits inferiores a 32 000 y 5 o más paquetes por segundo para velocidades de bits mayores o iguales que 32000.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la codificación de audio](configuringaudioencoding.md)
</dt> <dt>

[Enumeración de tipos de audio para modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



