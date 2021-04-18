---
title: Entradas, secuencias y salidas
description: Entradas, secuencias y salidas
ms.assetid: f9f979c4-a15c-4f2a-b63c-7fe776394fdd
keywords:
- Windows Media Format SDK, entradas
- Windows Media Format SDK, secuencias
- Windows Media Format SDK, salidas
- Advanced Systems Format (ASF), INPUTS
- ASF (formato de sistemas avanzados), entradas
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- Advanced Systems Format (ASF), salidas
- ASF (formato de sistemas avanzados), salidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e6b6941a990b108c16b49648ec0d8d028a44d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704753"
---
# <a name="inputs-streams-and-outputs"></a>Entradas, secuencias y salidas

Una "entrada" en esta documentación es cualquier flujo de datos multimedia digital (como audio o vídeo) que la aplicación envía al objeto escritor desde un origen mediante las API adecuadas. Las entradas deben entregarse en un formato compatible. Se admiten varios formatos estándar de RGB y YUV como entrada, y los códecs de audio admiten PCM. Si el códec no admite de forma nativa un formato de entrada especificado, el objeto de escritor creará una instancia de un objeto auxiliar de audio o vídeo que sea capaz de convertir una gran variedad de formatos en formatos que el códec pueda aceptar. En el caso de las entradas de audio, el objeto auxiliar ajustará la profundidad de bits, la velocidad de muestreo y el número de canales según sea necesario. En el caso de las entradas de vídeo, el objeto auxiliar de vídeo realizará las conversiones de espacio de color y los ajustes de tamaño del rectángulo. En algunos casos, los datos de audio y vídeo comprimidos se pueden pasar en un flujo de entrada. Una entrada puede ser de algún otro tipo de medio además de audio y vídeo, como texto, comandos de script, imágenes fijas o datos de archivo arbitrarios.

Una "salida" en esta documentación hace referencia a los datos que el objeto de lector pasa a una aplicación para su representación. Una salida equivale a una sola secuencia en el momento de la reproducción. Si usa la exclusión mutua, todos los flujos mutuamente excluyentes comparten una sola salida. Normalmente, los datos de salida están en forma de datos de vídeo o audio sin comprimir, aunque pueden contener cualquier tipo de datos. Los formatos de salida de vídeo admitidos se muestran en otra parte de esta documentación.

El término "Stream" en esta documentación hace referencia a los datos de un archivo ASF, en lugar de (1) los datos de origen de entrada antes de que los procese el objeto de escritor, y (2) los datos de salida una vez descomprimidos por el objeto lector. Una secuencia ASF contiene datos que proceden de una única entrada en el objeto escritor, aunque se puede crear más de una secuencia a partir de la misma entrada. Un flujo tiene el mismo formato y la misma configuración de compresión de principio a fin. Un archivo ASF sencillo tiene dos flujos, uno para el audio y otro para el vídeo. Un archivo más complejo podría tener dos secuencias de audio y varias secuencias de vídeo. Los flujos de audio pueden tener la misma configuración de compresión pero contienen contenido diferente, como una narración en distintos idiomas. Es posible que las secuencias de vídeo contengan el mismo contenido, pero que tengan una configuración de compresión diferente. El formato de medios y la configuración de compresión que el objeto de escritor aplicará a cada flujo se especifican en el perfil.

La relación entre las entradas, las secuencias y las salidas puede ser de tres tipos básicos. Los tres diagramas siguientes ilustran las relaciones.

En la relación más básica, que es un perfil sin exclusión mutua, cada entrada se procesa mediante el escritor y se inserta en el archivo ASF como una única secuencia. En la reproducción, el lector lee la secuencia y entrega los ejemplos sin comprimir como una salida única, tal como se muestra en el diagrama siguiente.

![diagrama que muestra la relación normal entre las entradas, las secuencias y las salidas.](images/formatsdk03.png)

Una relación más compleja se produce cuando se usa una exclusión mutua de velocidad de bits múltiple. En este caso, el escritor procesa una única entrada y se codifica en varias velocidades de bits. Cada codificación de los datos se inserta en el archivo ASF como una secuencia independiente. En la reproducción, el lector determina la secuencia que se va a descomprimir en función del ancho de banda disponible. A continuación, el lector lee el flujo seleccionado y entrega los ejemplos sin comprimir como una salida única, tal como se muestra en el diagrama siguiente.

![diagrama que muestra las relaciones entre las entradas, las secuencias y las salidas cuando se usa la exclusión mutua de velocidad de bits múltiple.](images/formatsdk04.png)

El tercer tipo de relación puede producirse cuando se usa una exclusión mutua personalizada o basada en el lenguaje. En esta relación, el lector procesa varias entradas y cada una se inserta en el archivo ASF como una secuencia individual. En la reproducción, la aplicación selecciona manualmente la secuencia que se va a descomprimir en función de la lógica proporcionada. A continuación, el lector lee el flujo seleccionado y entrega los ejemplos sin comprimir como una salida única. Este proceso se puede usar para incluir bandas sonoras en varios idiomas. En el siguiente diagrama se muestra este proceso.

![diagrama que muestra las relaciones entre las entradas, las secuencias y las salidas cuando se usa la exclusión mutua personalizada.](images/formatsdk02.png)

Hay algunas variaciones en las relaciones descritas anteriormente. Por ejemplo, un archivo puede contener las tres relaciones, o una o dos de ellas. También es posible comprimir algunas entradas, en cuyo caso el escritor no realiza ninguna compresión adicional. El lector, también, puede proporcionar ejemplos comprimidos. Pero cuando lo hace, debe tener acceso a ellos por número de secuencia, no por número de salida.

> [!Note]  
> Los objetos del SDK de Windows Media Format tienen todos los números asignados a las entradas, los vapores y las salidas. Los flujos tienen un número de secuencia, que se basa en 1, que se define en el perfil. Cada flujo también se asigna a un índice de flujo para su uso en la enumeración de secuencias de un perfil. No se garantiza que ninguno de estos números sea coherente entre sí. Es decir, el número de entrada 1 puede no coincidir con el número de secuencia 1, el número de secuencia 1 puede no coincidir con el índice de flujo 1, etc.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Exclusión mutua**](mutual-exclusion.md)
</dt> </dl>

 

 




