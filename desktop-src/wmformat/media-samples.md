---
title: Ejemplos de medios (Windows SDK de formato multimedia 11)
description: Obtenga información sobre los ejemplos de medios en el SDK Windows Media Format 11. Un ejemplo multimedia es un objeto que contiene una lista ordenada de cero o más búferes.
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows SDK de formato multimedia, ejemplos de medios
- Windows SDK de formato multimedia, ejemplos
- Formato de sistemas avanzados (ASF), ejemplos multimedia
- ASF (formato de sistemas avanzados), ejemplos multimedia
- Formato de sistemas avanzados (ASF), ejemplos
- ASF (formato de sistemas avanzados), ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8d264aa23e80f1e692f28789c2f2e631ef3ed8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267028"
---
# <a name="media-samples-windows-media-format-11-sdk"></a>Ejemplos de medios (Windows SDK de formato multimedia 11)

Un ejemplo multimedia, o ejemplo, es un bloque de datos multimedia digitales. Un ejemplo es la unidad básica manipulada por los objetos de lectura y escritura del SDK Windows Media Format. El contenido de una muestra individual viene determinado por el tipo de medio asociado a la muestra. En el caso del vídeo, cada ejemplo representa un único fotograma. En el caso del audio, la cantidad de datos de un ejemplo individual se establece en el perfil utilizado para crear el archivo ASF.

Las muestras pueden contener datos sin comprimir o pueden contener datos comprimidos, en cuyo caso se denominan *ejemplos de secuencia.* Al crear un archivo ASF, se pasan ejemplos al escritor. El sistema de escritura coordina la compresión de los ejemplos con el códec adecuado y organiza los datos comprimidos en la sección de datos del archivo ASF. Durante la reproducción, el lector lee los datos comprimidos, los descomprime y proporciona los datos reconstruidos sin comprimir como ejemplos de salida.

Todos los ejemplos usados por Windows SDK de formato multimedia se encapsulan en el objeto de búfer cuya memoria se asigna automáticamente por los componentes en tiempo de ejecución del SDK. También puede asignar sus propios búferes si es necesario, mediante las características avanzadas del escritor y el lector.

**Nota** El término ejemplo se usa en este SDK para hacer referencia a un ejemplo multimedia, no a un ejemplo de audio. En la codificación de audio, un ejemplo hace referencia a un único valor de audio codificado. Normalmente, la calidad del audio codificado se especifica mediante un número de muestras por segundo. Por ejemplo, el sonido de calidad de CD se registra en 44 100 muestras por segundo. Este valor se abrevia normalmente con la notación Hz, por lo que 44 100 muestras por segundo serían 44 100 Hz o 44,1 kHz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Interfaz INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Entradas, Secuencias salidas**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




