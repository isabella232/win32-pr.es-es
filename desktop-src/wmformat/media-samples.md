---
title: Ejemplos de medios (Windows Media Format 11 SDK)
description: Ejemplos de medios
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- SDK de Windows Media Format, ejemplos de medios
- SDK de Windows Media Format, ejemplos
- Advanced Systems Format (ASF), ejemplos de medios
- ASF (formato de sistemas avanzados), ejemplos de medios
- Advanced Systems Format (ASF), ejemplos
- ASF (formato de sistemas avanzados), ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d46a933775877f4566115ba3936c0f9f8bd7b3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103995874"
---
# <a name="media-samples-windows-media-format-11-sdk"></a>Ejemplos de medios (Windows Media Format 11 SDK)

Un ejemplo multimedia, o ejemplo, es un bloque de datos multimedia digitales. Un ejemplo es la unidad básica que manipulan los objetos de lectura y escritura del SDK de Windows Media Format. El contenido de un ejemplo individual viene determinado por el tipo de medio asociado al ejemplo. En el caso de vídeo, cada ejemplo representa un solo fotograma. En el caso de audio, la cantidad de datos de un ejemplo individual se establece en el perfil que se usa para crear el archivo ASF.

Los ejemplos pueden contener datos sin comprimir o pueden contener datos comprimidos, en cuyo caso se denominan *ejemplos de secuencias*. Al crear un archivo ASF, se pasan ejemplos al escritor. El escritor coordina la compresión de los ejemplos con el códec adecuado y organiza los datos comprimidos en la sección de datos del archivo ASF. En la reproducción, el lector Lee los datos comprimidos, los descomprime y proporciona los datos sin comprimir reconstruidos como ejemplos de salida.

Todos los ejemplos utilizados por el SDK de Windows Media Format se encapsulan en un objeto de búfer cuya memoria se asigna automáticamente por los componentes en tiempo de ejecución del SDK. También puede asignar sus propios búferes si es necesario, con las características avanzadas del escritor y del lector.

**Nota:** El término ejemplo se usa en este SDK para hacer referencia a un ejemplo multimedia, no a un ejemplo de audio. En la codificación de audio, un ejemplo hace referencia a un único valor de audio codificado. Normalmente, la calidad del audio codificado se especifica mediante un número de muestras por segundo. Por ejemplo, el sonido de la calidad del CD se graba en 44.100 muestras por segundo. Este valor suele abreviarse con la notación de Hz, por lo que 44.100 muestras por segundo serían de 44.100 Hz o 44,1 kHz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Interfaz INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Entradas, secuencias y salidas**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




