---
description: En este tema se describe cómo Media Foundation transformaciones deben controlar las marcas de tiempo.
ms.assetid: 4ab576ce-becd-4736-921e-e463c0dff841
title: Marcas de tiempo y duraciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22452e8b6b8094e643126f479f13b2c447db584588f3be1c1aa6595b3e7e2bb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953205"
---
# <a name="time-stamps-and-durations"></a>Marcas de tiempo y duraciones

En este tema se describe [cómo Media Foundation transformaciones deben](media-foundation-transforms.md) controlar las marcas de tiempo.

Un MFT debe establecer una marca de tiempo y una duración lo más precisas posibles en todos los ejemplos de salida. Para un MFT simple que toma un búfer de entrada y lo procesa completamente en un búfer de salida, el MFT solo debe copiar la marca de tiempo y la duración directamente desde la muestra de entrada al ejemplo de salida. Sin embargo, muchas transformaciones son más complejas que esto y pueden requerir cálculos más complejos del tiempo de salida. Todas las MTA deben observar las siguientes reglas básicas:

-   Un MFT debe intentar colocar una marca de tiempo y una duración en todos los ejemplos de salida de audio o vídeo sin comprimir si se da una marca de tiempo o duración precisas en los ejemplos de entrada o se puede calcular. La interpolación puede ser necesaria para algunas marcas de tiempo de salida, especialmente para los descodificadores.
-   Las marcas de tiempo y las duraciones de los ejemplos de entrada deben conservarse tanto como sea posible en los ejemplos de salida.
-   Es posible que las marcas de tiempo o duraciones de salida no coincidan con la entrada porque el MFT retiene los datos o divide la salida en partes de diferente tamaño que la entrada. En ese caso, MFT debe calcular la marca de tiempo de salida a partir de la muestra de entrada más temprana que contiene los datos usados para crear el ejemplo de salida. Para calcular la marca de tiempo de salida, agregue la marca de tiempo de entrada de la muestra de entrada adecuada a la duración de los datos que ya se han transformado a partir de esa muestra. El segundo ejemplo al final de esta sección ilustra esta idea.
-   Si las muestras de entrada tienen duración, se debe conservar esa duración. Si una muestra de entrada no tiene duración, MFT debe calcular una duración si es posible a partir del tamaño del búfer de salida o la velocidad de datos que proporciona el tipo de medio.
-   Las duraciones calculadas se deben truncar (redondear hacia abajo), no redondeadas al incremento más cercano. La canalización tiene suficiente espacio para controlar duraciones que son ligeramente imprecisas, pero es más fácil para la canalización controlar una duración que es un 1 % demasiado corta que una duración que es un 1 % demasiado larga. Dicho esto, no hay ninguna razón para acortar deliberadamente las duraciones, aparte de redondear.

### <a name="decoders"></a>Decodificadores

Un descodificador convierte paquetes comprimidos en datos sin comprimir. Dado que la salida no está comprimida, los descodificadores tienen una obligación especial de obtener las marcas de tiempo y las duraciones correctas. Algunos formatos comprimidos, especialmente MPEG-2, no tienen marcas de tiempo en todos los paquetes de entrada y a menudo no tienen ninguna duración en ningún paquete. Para estos formatos, el descodificador es responsable de colocar una marca de tiempo y una duración válidas en cada muestra de salida, sumando las duraciones implícitas de toda la salida desde la última muestra de entrada con marca de tiempo.

En el caso del vídeo, si la duración no está disponible en el formato comprimido, el descodificador debe calcular la duración como la inversa de la velocidad de fotogramas, convertida a unidades de 100 nanosegundos y redondeada hacia abajo.

Para el audio, si la duración no está disponible en el formato comprimido, el descodificador debe calcular la duración como la inversa de la frecuencia de muestreo de audio multiplicada por el número de muestras en el búfer de salida, convertida a unidades de 100 nanosegundos y redondeada hacia abajo.

La única vez que una transformación debe generar una muestra sin marca de tiempo es si el MFT nunca ha recibido una marca de tiempo en una muestra de entrada o si no hay ninguna manera de calcular una marca de tiempo de salida precisa a partir de la marca de tiempo de entrada anterior.

### <a name="audio-decoders"></a>Descodificadores de audio

Para los descodificadores de audio, la duración de cada muestra de salida se calcula a partir de la frecuencia de muestreo de audio y el número de muestras de PCM por canal en el búfer de salida.

La manera correcta de calcular las marcas de tiempo de salida depende de si las muestras de entrada contienen marcas de tiempo.

Si los ejemplos de entrada contienen marcas de tiempo, el descodificador calcula las marcas de tiempo de salida a partir de las marcas de tiempo de entrada, como se muestra a continuación:

-   Si cada búfer de entrada contiene uno o varios fotogramas comprimidos completos, sin fotogramas parciales, la marca de tiempo de salida es igual a la marca de tiempo de entrada, menos la latencia conocida del descodificador. Por ejemplo, un descodificador Dolby Digital (AC-3) tiene una latencia de 256 ejemplos de PCM. Por ejemplo, a una velocidad de muestreo de 48 kHz, la latencia es de 5,33 milisegundos (ms). Por lo tanto, si la marca de tiempo de entrada es de 1000 ms, la marca de tiempo de salida es 1000 – 5,33 = 994,66 ms. Si el búfer de entrada incluye más de un marco comprimido completo, el descodificador producirá una muestra de salida para cada fotograma de la muestra de entrada. Todas las muestras de salida se marcarán correctamente para que no haya espacios.
-   Dependiendo del formato de transporte, un búfer de entrada puede contener fotogramas parciales. Por ejemplo, un búfer podría contener parte de un marco del búfer de entrada anterior, seguido de uno o varios fotogramas completos, seguido del inicio del fotograma siguiente. En este caso, por lo general es correcto suponer que la marca de tiempo de entrada corresponde al primer fotograma que se inicia dentro del búfer. (Es decir, un marco parcial que se inició en el búfer anterior no se incluye en la marca de tiempo del búfer actual). Calcule la marca de tiempo de salida en consecuencia.

Si los ejemplos de entrada no contienen marcas de tiempo:

-   El descodificador debe generar sus propias marcas de tiempo, estableciendo la primera marca de tiempo de salida en cero.
-   La duración de la muestra se calcula a partir del número de muestras de salida en el búfer y la frecuencia de muestreo.
-   Las marcas de tiempo posteriores se calculan a partir de la marca de tiempo y la duración anteriores: Marca de tiempo actual + duración actual = marca de tiempo siguiente. No debería haber espacios en las marcas de tiempo de salida.

Si el flujo de entrada contiene inicialmente marcas de tiempo, pero por algún motivo cambia a ninguna marca de tiempo, el descodificador debe seguir generando sus propias marcas de tiempo de salida, de modo que sean continuas y no haya ninguna brecha.

Si el flujo de entrada contiene marcas de tiempo, pero hay lagunas en los tiempos, el descodificador simplemente propagará estas brechas. En otras palabras, el descodificador no debe intentar corregir marcas de tiempo incoherentes en el flujo de entrada.

### <a name="mixers"></a>Mezcladores

> [!Note]  
> En Windows Vista, la canalización Media Foundation no admite MTA con más de una entrada. Las MTA de varias entradas se admiten en Windows 7.

 

Un mezclador toma varias entradas y las mezcla en una salida. Si los flujos de entrada no están completamente bloqueados por velocidad o se desplazan ligeramente en el tiempo entre sí, puede haber ambigüedad sobre el tiempo que se debe establecer en la salida. Estas son algunas directrices, en función del tipo de medio:

-   Audio. En el inicio o inmediatamente después de una purga o vaciado, un mezclador de audio debe esperar para generar muestras de salida hasta que haya recibido una muestra de entrada en todos los flujos de entrada necesarios. En ese momento, debe elegir la marca de tiempo más temprana de las muestras iniciales que se usarán como línea base para las marcas de tiempo de salida. Las demás secuencias se deben agregar con silencio para que se puedan crear discrepancias en cualquier momento. Si se recibe un ejemplo en un flujo de entrada opcional, también se debe tener en cuenta en el cálculo. A partir de ese momento, MFT debe procurar generar una cadena continua e ininterrumpida de marcas de tiempo de salida. En general, MFT no debe intentar tener en cuenta un flujo que se desvia con respecto a otro. En su lugar, debe calcular las marcas de tiempo de salida a partir de la marca de tiempo de línea de base, la velocidad de salida y los tamaños de búfer. Cuando se produce otro vaciado o purga, MFT debe restablecer sus marcas de tiempo de línea base.

-   Video. En el inicio o inmediatamente después de una purga o vaciado, un mezclador de vídeo debe esperar para generar muestras de salida hasta que haya recibido una muestra de entrada en todos los flujos de entrada necesarios. En ese momento, debe elegir la marca de tiempo más temprana de las muestras iniciales que se usarán como línea base para las marcas de tiempo de salida. En general, debe procurar mantener marcas de tiempo de salida continuas y regulares y duraciones fijas, incluso si la entrada no es tan normal, si es necesario mediante la repetición de fotogramas de entrada.

### <a name="encoders"></a>Codificadores

Un codificador convierte audio o vídeo sin comprimir en paquetes comprimidos. Un codificador debe seguir estas directrices:

-   El codificador debe seguir las convenciones del formato de salida. Si el formato no suele marca de tiempo en todas las muestras, como en MPEG-2, no todas las muestras de salida deben tener una marca de tiempo y una duración.

-   Las marcas de tiempo de entrada deben conservarse en el formato de salida, si el formato tiene campos para las marcas de tiempo, a menos que la información de hora mejor esté disponible desde otro origen, como la propia aplicación.

### <a name="multiplexers"></a>Multiplexores

> [!Note]  
> En Windows Vista, la canalización Media Foundation no admite MTA con más de una entrada. Las MTA de varias entradas se admiten en Windows 7.

 

Un multiplexor combina dos secuencias de audio o vídeo diferentes en un formato intercalado, como AVI o MPEG-2 Transport Stream. Un multiplexor debe seguir estas directrices:

-   El multiplexor debe seguir las convenciones del formato de salida. Si el formato no suele marca de tiempo en todas las muestras, como en MPEG-2, no todas las muestras de salida deben tener una marca de tiempo y una duración.

-   La marca de tiempo debe reflejar la hora más temprana que se colocaría en cualquier fotograma que comience en ese paquete, o la hora de la primera muestra de audio que se descodificaría a partir de ese paquete. O bien, si entra en conflicto con las convenciones del formato de salida.

### <a name="demultiplexers"></a>Demultiplexores

Un demultiplexor divide un formato intercalado, como AVI o MPEG-2 Transport Stream, en las secuencias de audio y vídeo subyacentes.

Si el formato contiene información de marca de tiempo específica que se puede usar para calcular marcas de tiempo de salida precisas en función de las marcas de tiempo de entrada, se debe usar esa información. Sin embargo, si el formato contiene horas en una base completamente diferente que no tienen ninguna relación con las marcas de tiempo de entrada y no se puede calcular un desplazamiento preciso de la marca de tiempo de entrada, se deben omitir las horas propias del formato.

Si el formato no tiene información de marca de tiempo utilizable, el demultiplexor debe seguir estas reglas:

-   Los flujos de salida sin comprimir deben tener marcas de tiempo y duraciones válidas, si es posible, calculadas a partir de la marca de tiempo de entrada anterior más cercana.

-   Los flujos de salida comprimidos deben tener marcas de tiempo solo en la primera muestra de salida derivada de una muestra de entrada con una marca de tiempo. Si el ejemplo de entrada no tiene una marca de tiempo, ninguna muestra de salida derivada de esa muestra de entrada debe tener una marca de tiempo. Si la muestra de entrada se divide en varios ejemplos de salida, solo la primera muestra de salida debe tener una marca de tiempo y el resto no debe tener marcas de tiempo.

### <a name="examples"></a>Ejemplos

Ejemplo 1. Supongamos que un efecto de vídeo siempre toma un marco de entrada sin comprimir, aplica el efecto y lo copia en la salida. Nunca retene los fotogramas ni almacena en búfer ninguna entrada. Este MFT simplemente copia la marca de tiempo y la duración de la muestra de entrada en la muestra de salida, si están disponibles, y no realiza ningún cálculo de tiempo.

Ejemplo 2. Supongamos que un efecto de audio transforma todos los menos 10 milisegundos (ms) de cada búfer de entrada, guardando los 10 ms adicionales para combinar con el búfer siguiente. Obtiene una secuencia de muestras que tienen una duración de 50 ms. Los tiempos de entrada se muestran en la tabla siguiente.



| Muestra | Tiempo de entrada | Duración de la entrada | Hora de salida | Duración de la salida |
|--------|------------|----------------|-------------|-----------------|
| 1      | 20         | 50             | 20          | 40              |
| 2      | 70         | 50             | 60          | 50              |
| 3      | 121        | 50             | 110         | 50              |
| 4      | 171        | 50             | 161         | 50              |



 

Observe la discrepancia de 1 ms entre la duración real de la muestra 2 y la duración implícita en función de la siguiente marca de tiempo (121 ? 70 = 51).

Dado que MFT retene 10 ms, genera los primeros 40 ms de la muestra de entrada 1 como ejemplo de salida 1, con una marca de tiempo de 20 ms y una duración de 40 ms.

El ejemplo de salida 2 combina los 10 ms previamente retenidos con 40 ms de la muestra de entrada 2. A este ejemplo se le proporciona una marca de tiempo de 60 ms (la marca de tiempo de la muestra de entrada anterior, 20 ms, más la duración de los datos ya procesados a partir de esa muestra, 40 ms). Se le da una duración de 50 ms.

De forma similar, el ejemplo siguiente tiene una marca de tiempo de 110 ms (70 ms + 40 ms) con una duración de 50 ms.

El siguiente cálculo es más interesante. La marca de tiempo implícita del tiempo y la duración de salida anteriores sería de 160 ms (marca de tiempo de 110 ms + duración de 50 ms). Sin embargo, se supone que la marca de tiempo de salida se calcula a partir de la marca de tiempo de entrada de la muestra de entrada más temprana que se superpone a la muestra de salida en el tiempo, además de la longitud de los datos ya procesados a partir de esa muestra. La muestra de entrada superpuesta más cercana es la muestra 4 (marca de tiempo = 171), pero esta no es la más temprana. La muestra superpuesta más temprana es la muestra 3 (marca de tiempo = 121). Al agregar los 40 ms que ya se han procesado a partir de ese ejemplo, el resultado es 161.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritura de un MFT personalizado](writing-a-custom-mft.md)
</dt> </dl>

 

 



