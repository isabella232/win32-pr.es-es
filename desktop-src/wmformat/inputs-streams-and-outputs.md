---
title: Entradas, Secuencias salidas
description: Entradas, Secuencias salidas
ms.assetid: f9f979c4-a15c-4f2a-b63c-7fe776394fdd
keywords:
- Windows SDK de formato multimedia, entradas
- Windows SDK de formato multimedia, secuencias
- Windows SDK de formato multimedia, salidas
- Formato de sistemas avanzados (ASF), entradas
- ASF (formato de sistemas avanzados), entradas
- Formato de sistemas avanzados (ASF),streams
- ASF (formato de sistemas avanzados), secuencias
- Formato de sistemas avanzados (ASF), salidas
- ASF (formato de sistemas avanzados), salidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e6b6941a990b108c16b49648ec0d8d028a44d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466707"
---
# <a name="inputs-streams-and-outputs"></a>Entradas, Secuencias salidas

Una "entrada" en esta documentación es cualquier flujo de datos multimedia digital (como audio o vídeo) que la aplicación entrega al objeto de escritor desde un origen mediante las API adecuadas. Las entradas deben entregarse en un formato compatible. Se admiten varios formatos RGB y YUV estándar como entrada, y los códecs de audio admiten PCM. Si el códec no admite de forma nativa un formato de entrada especificado, el objeto de escritor crea una instancia de un objeto auxiliar de audio o vídeo capaz de convertir una amplia variedad de formatos en formatos que el códec puede aceptar. En el caso de las entradas de audio, el objeto auxiliar ajustará la profundidad de bits, la frecuencia de muestreo y el número de canales según sea necesario. En el caso de las entradas de vídeo, el objeto auxiliar de vídeo realizará conversiones de espacio de color y ajustes de tamaño de rectángulo. En algunos casos, los datos comprimidos de audio y vídeo se pueden pasar en un flujo de entrada. Una entrada puede ser de otro tipo de medio, además de audio y vídeo, como texto, comandos de script, imágenes fijas o datos de archivo arbitrarios.

Una "salida" de esta documentación hace referencia a los datos que el objeto de lector pasa a una aplicación para su representación. Una salida equivale a una sola secuencia en el momento de la reproducción. Si usa la exclusión mutua, todas las secuencias mutuamente excluyentes comparten una única salida. Normalmente, los datos de salida tienen la forma de datos de audio o vídeo sin comprimir, aunque pueden contener cualquier tipo de datos. Los formatos de salida de vídeo admitidos se muestran en otra parte de esta documentación.

El término "secuencia" de esta documentación hace referencia a los datos de un archivo ASF, en lugar de (1) los datos de origen de entrada antes de que los procese el objeto de escritor y (2) los datos de salida después de que el objeto de lector los descomprima. Una secuencia de ASF contiene datos que proceden de una sola entrada en el objeto de escritor, aunque se puede crear más de una secuencia a partir de la misma entrada. Una secuencia tiene la misma configuración de formato y compresión de principio a fin. Un archivo ASF simple tiene dos secuencias, una para audio y otra para vídeo. Un archivo más complejo podría tener dos secuencias de audio y varias secuencias de vídeo. Las secuencias de audio pueden tener la misma configuración de compresión, pero contienen contenido diferente, como una narración en distintos idiomas. Las secuencias de vídeo pueden contener el mismo contenido, pero tienen una configuración de compresión diferente. La configuración de formato multimedia y compresión que el objeto de escritor aplicará a cada secuencia se especifican en el perfil.

La relación entre entradas, flujos y salidas puede ser de tres tipos básicos. Los tres diagramas siguientes ilustran las relaciones.

En la relación más básica, que es un perfil sin exclusión mutua, el escritor procesa cada entrada y se inserta en el archivo ASF como una sola secuencia. Durante la reproducción, el lector lee la secuencia y entrega muestras sin comprimir como una única salida, como se muestra en el diagrama siguiente.

![diagrama que muestra la relación normal entre entradas, flujos y salidas.](images/formatsdk03.png)

Se produce una relación más compleja cuando se usa la exclusión mutua de varias velocidades de bits. En este caso, el escritor procesa una única entrada y se codifica a varias velocidades de bits. Cada codificación de los datos se inserta en el archivo ASF como una secuencia independiente. En la reproducción, el lector determina qué secuencia se va a descomprimir en función del ancho de banda disponible. A continuación, el lector lee la secuencia seleccionada y entrega muestras sin comprimir como una única salida, como se muestra en el diagrama siguiente.

![diagrama que muestra las relaciones entre entradas, flujos y salidas cuando se usa la exclusión mutua de varias velocidades de bits.](images/formatsdk04.png)

El tercer tipo de relación puede producirse cuando se usa una exclusión mutua personalizada o basada en lenguaje. En esta relación, el lector procesa varias entradas y cada una de ellas se inserta en el archivo ASF como una secuencia individual. En la reproducción, la aplicación selecciona manualmente qué secuencia se va a descomprimir en función de la lógica que proporcione. A continuación, el lector lee la secuencia seleccionada y entrega muestras sin comprimir como una única salida. Este proceso se puede usar para incluir las versiones en varios idiomas. En el siguiente diagrama se muestra este proceso.

![diagrama que muestra las relaciones entre entradas, flujos y salidas cuando se usa la exclusión mutua personalizada.](images/formatsdk02.png)

Hay alguna variación en las relaciones descritas anteriormente. Por ejemplo, un archivo puede contener las tres relaciones, o una o dos de ellas. También es posible comprimir algunas entradas, en cuyo caso el escritor no realiza ninguna compresión adicional. El lector también puede entregar muestras comprimidas. Pero cuando lo haga, debe acceder a ellos por número de secuencia, no por número de salida.

> [!Note]  
> Las entradas, los movimientos y las salidas son números asignados por los objetos del SDK Windows Media Format. Secuencias un número de secuencia, que se basa en 1, que se define en el perfil. A cada secuencia también se le asigna un índice de secuencia para su uso en la enumeración de secuencias en un perfil. No se garantiza que ninguno de estos números sea coherente entre sí. Es decir, es posible que el número de entrada 1 no se corresponda con el número de secuencia 1, que el número de secuencia 1 no se corresponda con el índice de flujo 1, y así sucesivamente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> <dt>

[**Exclusión mutua**](mutual-exclusion.md)
</dt> </dl>

 

 




