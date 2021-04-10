---
description: En este tema se describe cómo las transformaciones de Media Foundation deben controlar las marcas de tiempo.
ms.assetid: 4ab576ce-becd-4736-921e-e463c0dff841
title: Marcas de tiempo y duraciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2323c11fa0e3ec2b2b2d5ba1cefe4f5d5fa80c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155312"
---
# <a name="time-stamps-and-durations"></a>Marcas de tiempo y duraciones

En este tema se describe cómo las [transformaciones de Media Foundation](media-foundation-transforms.md) deben controlar las marcas de tiempo.

Una MFT debe establecer una marca de tiempo y una duración como sea posible en todos los ejemplos de salida. En el caso de un MFT sencillo que toma un búfer de entrada y lo procesa completamente en un búfer de salida, la MFT solo debe copiar la marca de tiempo y la duración directamente de la muestra de entrada en el ejemplo de salida. Sin embargo, muchas transformaciones son más complejas que esta y pueden requerir cálculos más complejos de tiempo de salida. Todos los MFTs deben cumplir las siguientes reglas básicas:

-   Una MFT debe intentar colocar una marca de tiempo y una duración en todos los ejemplos de salida de vídeo o audio sin comprimir si se proporciona una marca de tiempo o una duración precisas en los ejemplos de entrada o se puede calcular. La interpolación puede ser necesaria para algunas marcas de tiempo de salida, especialmente para los descodificadores.
-   Las marcas de tiempo y las duraciones de los ejemplos de entrada deben conservarse en los ejemplos de salida tanto como sea posible.
-   Es posible que las marcas de tiempo de salida o las duraciones no coincidan con la entrada porque la MFT está reteniendo los datos o dividiendo la salida en partes de tamaño diferente que la entrada. En ese caso, el MFT debe calcular la marca de tiempo de salida del ejemplo de entrada más antiguo que contiene los datos usados para crear el ejemplo de salida. Para calcular la marca de tiempo de salida, agregue la marca de tiempo de entrada del ejemplo de entrada adecuado a la duración de los datos que ya se han transformado desde ese ejemplo. En el segundo ejemplo al final de esta sección se muestra esta idea.
-   Si los ejemplos de entrada tienen duración, se debe conservar esa duración. Si una muestra de entrada no tiene duración, la MFT debe calcular una duración si es posible a partir del tamaño del búfer de salida o la velocidad de datos proporcionada por el tipo de medio.
-   Las duraciones calculadas deben truncarse (redondearse hacia abajo), no redondeadas al incremento más próximo. La canalización tiene suficiente demora para controlar las duraciones que son ligeramente inexactas, pero es más fácil que la canalización controle una duración de un 1% demasiado corta que una duración de 1% demasiado larga. Dicho esto, no hay ningún motivo para acortar deliberadamente las duraciones, aparte de redondear.

### <a name="decoders"></a>Descodificadores

Un descodificador convierte los paquetes comprimidos en datos sin comprimir. Dado que la salida está sin comprimir, los descodificadores tienen una obligación especial de obtener las marcas de tiempo y las duraciones correctas. Algunos formatos comprimidos, en especial MPEG-2, no tienen marcas de tiempo en todos los paquetes entrantes y, a menudo, no tienen ninguna duración en ningún paquete. Para estos formatos, el descodificador es responsable de colocar una marca de tiempo y una duración válidas en cada ejemplo de salida, mediante la suma de las duraciones implícitas de toda la salida desde el último ejemplo de entrada con marca de tiempo.

En el caso de vídeo, si la duración no está disponible en el formato comprimido, el descodificador debe calcular la duración como inverso de la velocidad de fotogramas, convertido a unidades de 100-nanosegundos y redondeado hacia abajo.

En el caso de audio, si la duración no está disponible en el formato comprimido, el descodificador debe calcular la duración como el inverso de la velocidad de muestra de audio multiplicado por el número de muestras en el búfer de salida, convertido a unidades de 100-nanosegundos y redondeado hacia abajo.

La única vez que una transformación debe generar una muestra sin una marca de tiempo es si la MFT nunca ha recibido una marca de tiempo en una muestra de entrada, o si no hay ninguna manera de calcular una marca de tiempo de salida precisa de la marca de tiempo de entrada anterior.

### <a name="audio-decoders"></a>Descodificadores de audio

En el caso de los descodificadores de audio, la duración de cada ejemplo de salida se calcula a partir de la velocidad de muestreo de audio y el número de muestras de PCM por canal en el búfer de salida.

La manera correcta de calcular las marcas de tiempo de salida depende de si los ejemplos de entrada contienen marcas de tiempo.

Si los ejemplos de entrada contienen marcas de tiempo, el descodificador calcula las marcas de tiempo de salida a partir de las marcas de tiempo de entrada, como se indica a continuación:

-   Si cada búfer de entrada contiene uno o varios marcos comprimidos completos, sin fotogramas parciales, la marca de tiempo de salida es igual a la marca de tiempo de entrada, menos la latencia conocida del descodificador. Por ejemplo, un descodificador Dolby Digital (AC-3) tiene una latencia de ejemplos 256 PCM. Por ejemplo, con una frecuencia de muestreo de 48 kHz, la latencia es de 5,33 milisegundos (MS). Por lo tanto, si la marca de tiempo de entrada es de 1000 ms, la marca de tiempo de salida es 1000 – 5,33 = 994,66 ms. Si el búfer de entrada incluye más de un fotograma comprimido completo, el descodificador generará un ejemplo de salida para cada fotograma de la muestra de entrada. Todos los ejemplos de salida tendrán una marca de tiempo correctamente, de modo que no haya huecos.
-   Dependiendo del formato de transporte, un búfer de entrada podría contener fotogramas parciales. Por ejemplo, un búfer puede contener parte de un fotograma del búfer de entrada anterior, seguido de uno o varios marcos completos, seguido del inicio del fotograma siguiente. En este caso, generalmente es correcto asumir que la marca de tiempo de entrada corresponde al primer fotograma que se inicia dentro del búfer. (Es decir, un marco parcial que comenzó en el búfer anterior no se incluye en la marca de tiempo del búfer actual). Calcular la marca de tiempo de salida en consecuencia.

Si los ejemplos de entrada no contienen marcas de tiempo:

-   El descodificador debe generar sus propias marcas de tiempo y establecer la primera marca de tiempo de salida en cero.
-   La duración de ejemplo se calcula a partir del número de muestras de salida del búfer y la velocidad de muestra.
-   Las marcas de tiempo subsiguientes se calculan a partir de la marca de tiempo y la duración anteriores: marca de tiempo actual + duración actual = siguiente marca de tiempo. No debe haber huecos en las marcas de tiempo de salida.

Si el flujo de entrada contiene inicialmente marcas de tiempo, pero por algún motivo cambia a ninguna marca de tiempo, el descodificador debe continuar generando sus propias marcas de tiempo de salida, de modo que sean continuas y no haya ningún intervalo.

Si el flujo de entrada contiene marcas de tiempo, pero hay huecos en las horas, el descodificador simplemente propagará estos huecos. En otras palabras, el descodificador no debe intentar corregir las marcas de tiempo incoherentes en el flujo de entrada.

### <a name="mixers"></a>Mezcladores

> [!Note]  
> En Windows Vista, la canalización de Media Foundation no admite MFTs con más de una entrada. Se admiten MFTs de varias entradas en Windows 7.

 

Un mezclador toma varias entradas y las mezcla en una salida. Si los flujos de entrada no están totalmente bloqueados o se desplazan ligeramente en el tiempo entre sí, puede haber ambigüedad sobre el tiempo que se debe establecer en la salida. Estas son algunas instrucciones, según el tipo de medio:

-   Audio. En el inicio o inmediatamente después de una purga o vaciado, un mezclador de audio debe esperar para producir muestras de salida hasta que se haya recibido un ejemplo de entrada en todos los flujos de entrada necesarios. En ese momento, debe elegir la marca de tiempo más temprana de las muestras iniciales que se usará como línea base para las marcas de tiempo de salida. El resto de flujos se deben rellenar con un silencio para componer cualquier diferencia de tiempo. Si se recibe un ejemplo en un flujo de entrada opcional, también se debe factorizar en el cálculo. A partir de ese momento, la MFT debe procurar generar una cadena continua y no rota de marcas de tiempo de salida. En general, la MFT no debe intentar tener en cuenta una derivación de flujo relativa a otra. En su lugar, debe calcular las marcas de tiempo de salida a partir de la marca de tiempo de línea de base, la tasa de salida y los tamaños de búfer. Cuando se produce otra purga o vaciado, el MFT debe restablecer las marcas de tiempo de línea de base.

-   Video. En el inicio o inmediatamente después de una purga o vaciado, un mezclador de vídeo debe esperar para producir muestras de salida hasta que se haya recibido un ejemplo de entrada en todos los flujos de entrada necesarios. En ese momento, debe elegir la marca de tiempo más temprana de las muestras iniciales que se usará como línea base para las marcas de tiempo de salida. En general, debe procurar mantener marcas de tiempo de salida continuas y normales y duraciones fijas, incluso si la entrada no es tan regular, si es necesario, repitiendo los fotogramas de entrada.

### <a name="encoders"></a>Codificadores

Un codificador convierte audio o vídeo sin comprimir en paquetes comprimidos. Un codificador debe seguir estas instrucciones:

-   El codificador debe seguir las convenciones del formato de salida. Si el formato no suele ser una marca de tiempo en cada ejemplo, como en MPEG-2, no todos los ejemplos de salida deben tener una marca de tiempo y una duración.

-   Las marcas de tiempo de entrada deben conservarse en el formato de salida, si el formato tiene campos para las marcas de tiempo, a menos que haya más información de tiempo disponible de otro origen, como la propia aplicación.

### <a name="multiplexers"></a>Multiplexores

> [!Note]  
> En Windows Vista, la canalización de Media Foundation no admite MFTs con más de una entrada. Se admiten MFTs de varias entradas en Windows 7.

 

Un multiplexor combina dos secuencias de audio o vídeo diferentes en un formato intercalado, como la secuencia de transporte AVI o MPEG-2. Un multiplexor debe seguir estas instrucciones:

-   El multiplexor debe seguir las convenciones del formato de salida. Si el formato no suele ser una marca de tiempo en cada ejemplo, como en MPEG-2, no todos los ejemplos de salida deben tener una marca de tiempo y una duración.

-   La marca de tiempo debe reflejar la hora más temprana en que se colocaría en cualquier fotograma que comience en ese paquete o la hora de la primera muestra de audio que se descodificaría de ese paquete. Omita esta directriz si entra en conflicto con las convenciones del formato de salida.

### <a name="demultiplexers"></a>Demultiplexadores

Un desmultiplexador divide un formato intercalado, como un flujo de transporte AVI o MPEG-2, en las secuencias de audio y vídeo subyacentes.

Si el formato contiene información específica de la marca de tiempo que se puede usar para calcular las marcas de tiempo de salida precisas en función de las marcas de tiempo de entrada, se debe usar esa información. Sin embargo, si el formato contiene horas en una base completamente diferente que no tienen ninguna relación con las marcas de tiempo de entrada, y no se puede calcular un desplazamiento exacto de la marca de tiempo de entrada, se deben omitir las horas propias del formato.

Si el formato no tiene información de marca de tiempo utilizable, el demultiplexador debe seguir estas reglas:

-   Los flujos de salida sin comprimir deben tener marcas de tiempo y duraciones válidas si es posible, calculadas a partir de la marca de tiempo de entrada anterior más cercana.

-   Los flujos de salida comprimidos deben tener marcas de tiempo en el primer ejemplo de salida derivado de un ejemplo de entrada con una marca de tiempo. Si el ejemplo de entrada no tiene una marca de tiempo, ningún ejemplo de salida derivado de ese ejemplo de entrada debe tener una marca de tiempo. Si el ejemplo de entrada se divide en varios ejemplos de salida, solo el primer ejemplo de salida debe tener una marca de tiempo y el resto no debe tener ninguna marca de tiempo.

### <a name="examples"></a>Ejemplos

Ejemplo 1. Supongamos que un efecto de vídeo siempre toma un fotograma de entrada sin comprimir, aplica el efecto y lo copia en la salida. Nunca mantiene ningún fotograma ni almacena en búfer ninguna entrada. Este MFT simplemente copia la marca de tiempo y la duración de la muestra de entrada en el ejemplo de salida, si están disponibles, y no realiza cálculos de tiempo.

Ejemplo 2. Supongamos que un efecto de audio transforma todo menos de 10 milisegundos (MS) de cada búfer de entrada, guardando el 10 ms extra para combinarlo con el siguiente búfer. Obtiene una secuencia de ejemplos que tienen una duración de 50 ms. Los tiempos de entrada se muestran en la tabla siguiente.



| Muestra | Hora de entrada | Duración de entrada | Hora de salida | Duración de la salida |
|--------|------------|----------------|-------------|-----------------|
| 1      | 20         | 50             | 20          | 40              |
| 2      | 70         | 50             | 60          | 50              |
| 3      | 121        | 50             | 110         | 50              |
| 4      | 171        | 50             | 161         | 50              |



 

Tenga en cuenta la discrepancia de 1 ms entre la duración real del ejemplo 2 y la duración implícita según la siguiente marca de tiempo (121? 70 = 51).

Dado que la MFT contiene 10 ms, genera el primer 40 ms de la muestra de entrada 1 como muestra de salida 1, con una marca de tiempo de 20 MS y una duración de 40 ms.

El ejemplo de salida 2 combina los 10 ms previamente retenidos con 40 ms de la muestra de entrada 2. A este ejemplo se le asigna una marca de tiempo de 60 ms (la marca de tiempo de la muestra de entrada anterior, 20 MS, más la duración de los datos ya procesados de ese ejemplo, 40 ms). Se le asigna una duración de 50 ms.

Del mismo modo, el ejemplo siguiente tiene una marca de tiempo de 110ms (70ms + 40 ms) con una duración de 50 ms.

El siguiente cálculo es más interesante. La marca de tiempo implícita de la hora de salida y la duración anteriores sería 160 ms (marca de tiempo 110 MS + Duration 50 ms). Sin embargo, se supone que la marca de tiempo de salida se calcula a partir de la marca de tiempo de entrada del ejemplo de entrada más antiguo que se superpone a la muestra de salida en el tiempo, más la longitud de los datos ya procesados desde ese ejemplo. El ejemplo de entrada superpuesto más cercano es el ejemplo 4 (marca de tiempo = 171), pero no es el más antiguo. El ejemplo superpuesto más antiguo es Sample 3 (marca de tiempo = 121). Al agregar el 40 ms que ya se ha procesado desde ese ejemplo, el resultado es 161.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir una MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 



