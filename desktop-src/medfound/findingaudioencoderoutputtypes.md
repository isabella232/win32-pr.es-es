---
description: Búsqueda de tipos de salida del codificador de audio
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Búsqueda de tipos de salida del codificador de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5389274cca1178ebc0ae03e21f7a804f73a5db48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705406"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a>Búsqueda de tipos de salida del codificador de audio (Microsoft Media Foundation)

Dado que debe usar un formato de salida de codificador de audio que sea enumerado por el codificador de audio, debe tener una forma de encontrar el formato más adecuado para sus necesidades. El número de canales, bits por muestra y la velocidad de muestra de la salida que elija debe coincidir con los valores del contenido que comprime. Sin embargo, el codificador puede admitir varios tipos dentro de estas restricciones.

El factor decisivo para elegir un tipo es la velocidad de bits de la secuencia codificada; quiere buscar un tipo de medio que coincida con la entrada y que tenga una velocidad de bits lo más cercana posible a un valor de destino. Si está enumerando los tipos de salida VBR de un paso, es el valor de calidad que decidirá el tipo que utiliza. Para obtener más información sobre los valores de calidad de los tipos de salida enumerados, consulte [enumeración de tipos de audio para modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md).

> [!Note]  
>    El codificador de audio enumera algunos tipos que son duplicados de otros tipos de prácticamente todas formas. Estos duplicados existen para formatos en los que el número de paquetes por segundo no cumple los requisitos de almacenamiento en archivos ASF cuando se sincronizan con vídeo. El audio sincronizado con vídeo en un archivo ASF debe tener 3 o más paquetes por segundo para velocidades de bits inferiores a 32000 y 5 o más paquetes por segundo para velocidades de bits iguales o superiores a 32000.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la codificación de audio](configuringaudioencoding.md)
</dt> <dt>

[Enumeración de los tipos de audio para los modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



