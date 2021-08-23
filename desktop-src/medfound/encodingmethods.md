---
description: Métodos de codificación
ms.assetid: 17ab5ecc-0173-4c5c-9d65-40e506ab7e07
title: Métodos de codificación (Microsoft Media Foundation)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa11e9545aa38358e5e1c0fdb4dfc4b7a2c3ee13f24b0fa38fe76b9e8bddcc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974534"
---
# <a name="encoding-methods-microsoft-media-foundation"></a>Métodos de codificación (Microsoft Media Foundation)

La mayoría de los códecs Windows audio multimedia y vídeo admiten varios métodos de codificación. Saber cómo y cuándo usar cada método puede ayudarle a crear contenido comprimido de alta calidad.

Todos los métodos de codificación se centran en el búfer utilizado por el descodificador para administrar los datos de entrada comprimidos. Este búfer se define por la velocidad de bits de la secuencia, en bits por segundo, y la ventana del búfer, en milisegundos. Al codificar, el códec se rige por las restricciones del búfer. Para obtener más información sobre el búfer, vea [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).

## <a name="constant-bit-rate-encoding"></a>Codificación de velocidad de bits constante

La velocidad de bits de cualquier secuencia codificada por uno de los códecs Windows audio multimedia y vídeo no es constante. Por lo tanto, la codificación de velocidad de bits constante (CBR) es un término algo confuso. La característica distintiva de una secuencia codificada por CBR es una ventana de búfer pequeña, que limita la variación de los tamaños de muestra. La codificación CBR se usa principalmente para el contenido que se transmite a través de una red a su destino. En este escenario, es importante poder basarse en un uso coherente del ancho de banda.

Desde el punto de vista de la configuración, la codificación CBR difiere de los demás modos en que, antes de empezar a codificar, se establece tanto la velocidad de bits media del contenido de salida como la ventana de búfer que se aplica a esa velocidad de bits. En otros modos, uno o ambos valores son desconocidos al configurar el codificador y se calculan mediante el códec mientras codifica. CBR es el modo de codificación estándar que usa Windows DDO del codificador multimedia.

## <a name="two-pass-constant-bit-rate-encoding"></a>Two-Pass codificación de velocidad de bits constante

CBR estándar usa solo un paso de codificación único. El contenido se proporciona como ejemplos de entrada y el códec comprime el contenido y devuelve ejemplos de salida. También es posible procesar muestras de entrada dos veces. En el primer paso, el códec realiza cálculos para optimizar la codificación del contenido. En el segundo paso, el códec usa los datos recopilados durante el primer paso para codificar el contenido.

La codificación CBR de dos pases tiene muchas ventajas. A menudo produce importantes mejoras de calidad sobre la codificación CBR estándar sin cambiar ninguno de los requisitos de almacenamiento en búfer. Esto hace que este modo de codificación sea ideal para el contenido que se transmite a través de una red. La única situación en la que cbr de dos pases no es factible es cuando se codifica contenido desde un origen en directo y no se puede usar un segundo paso.

El tipo de medio de salida de una secuencia CBR de dos pases es idéntico al de una secuencia CBR estándar; sigue especificando la velocidad de bits y la ventana de búfer que se va a usar. Al configurar el DMO, debe establecerlo para realizar dos pases. Y debe notificar a la DMO cuando haya terminado de enviar ejemplos para el primer paso.

## <a name="quality-based-variable-bit-rate-encoding"></a>Quality-Based codificación de velocidad de bits variable

Dado que la codificación CBR no mantiene realmente una velocidad de bits constante, la distinción entre ella y la codificación de velocidad de bits variable (VBR) puede parecer un poco confusa. La diferencia principal entre CBR y VBR es el tamaño de la ventana de búfer utilizada. Las secuencias codificadas con VBR suelen tener ventanas de búfer grandes en comparación con las secuencias codificadas por CBR. LA VBR basada en la calidad no es una excepción, ya que no se define ni la velocidad de bits ni la ventana de búfer para él. En su lugar, establezca un valor de calidad. A continuación, el códec intenta comprimir los datos para que la calidad del medio codificado sea coherente a lo largo de su duración, independientemente de los requisitos de búfer de la secuencia resultante.

VBR basado en calidad usa un solo paso de codificación y tiende a crear secuencias comprimidas de gran tamaño. Una vez completada la codificación, el códec establece los requisitos del búfer para que el descodificador pueda descomprimir los datos. La secuencia de VBR codificada no es adecuada para el streaming a través de una red, por lo que VBR basado en la calidad solo debe usarse para escenarios de reproducción locales (o para descargar y reproducir).

## <a name="unconstrained-variable-bit-rate-encoding"></a>Codificación de velocidad de bits variable sin restricciones

A diferencia de VBR basado en calidad, VBR sin restricciones no codifica a un nivel de calidad específico. En su lugar, codifica el contenido con la máxima calidad posible mientras se mantiene una velocidad de bits especificada. VBR sin restricciones usa dos pases de codificación y es similar a CBR de dos pases, salvo que no se especifica una configuración de ventana de búfer para la secuencia. Esto significa que no hay ningún límite en el tamaño de muestras individuales en la secuencia, siempre y cuando la velocidad de bits media sea menor o igual que el valor establecido.

VBR sin restricciones es de uso limitado, ya que hay pocos escenarios de reproducción que tienen requisitos para cumplir con sus requisitos de búfer. El códec puede establecer la ventana del búfer en cualquier valor necesario después de la codificación, lo que no le da ningún control sobre el tamaño del búfer. En la mayoría de los casos, si no le preocupa el tamaño del búfer o la coherencia del uso del ancho de banda, debe usar VBR basado en calidad.

## <a name="peak-constrained-variable-bit-rate-encoding"></a>Peak-Constrained codificación de velocidad de bits variable

El modo de codificación final es VBR con restricciones máximas. Al igual que VBR sin restricciones, este modo usa dos pases de codificación y codifica a una velocidad de bits especificada. Sin embargo, con VBR con restricciones máximas, también se configura el valor máximo para la codificación. Los valores máximos son similares a los valores de configuración normales del búfer: hay una velocidad de bits máxima y una ventana de búfer máxima. El archivo se codifica para ajustarse a un búfer descrito por los valores máximos, con la condición de que la velocidad de bits media total de la secuencia sea igual o menor que el valor de velocidad de bits promedio que especifique.

VbR restringido puede ser difícil de conceptualizar. Esta es la manera más fácil de pensar en el modelo de almacenamiento en búfer usado. Supongamos que la secuencia es una secuencia CBR con la velocidad de bits máxima y la ventana de búfer máxima que se usa para definir el búfer. Normalmente, la velocidad de bits máxima es bastante alta. El codificador garantiza que el valor de velocidad de bits promedio esperado que indique se mantiene durante la duración de la secuencia. En cualquier punto concreto de la secuencia, se garantiza que la velocidad de bits media sea mayor que el tamaño total de la secuencia en bits dividido por la duración de la secuencia en segundos).

Considere el ejemplo siguiente: configure una secuencia con una velocidad de bits media de 16 000 bits por segundo, una velocidad de bits máxima de 48 000 bits por segundo y una ventana de búfer máxima de 3000 (3 segundos). El tamaño del búfer usado para la secuencia es de 144 000 bits (48 000 bits por segundo x 3 segundos) determinado por los valores máximos. El codificador comprime los datos para ajustarse a ese búfer. Además, la velocidad de bits media de la secuencia debe ser de 16 000 o menos. Si el codificador necesita crear algunas muestras muy grandes para controlar un segmento complejo de contenido, puede aprovechar el gran tamaño del búfer. Sin embargo, otras partes de la secuencia deben codificarse a una velocidad de bits inferior para reducir el promedio al nivel especificado.

La codificación VBR con límite máximo es útil para reproducir dispositivos con una capacidad de búfer finita y algunas restricciones de velocidad de datos. Un ejemplo común de esto es la codificación que se usa para los DVD.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la codificación VBR](usingvbrencoding.md)
</dt> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



