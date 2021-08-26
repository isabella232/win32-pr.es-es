---
title: Creación del efecto de eco
description: Creación del efecto de eco
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Reproductor de Windows Media complementos, método DoProcessOutput de ejemplo de Echo
- plug-ins,Echo sample DoProcessOutput (método DoProcessOutput de ejemplo de eco)
- complementos de procesamiento de señales digitales, método DoProcessOutput de ejemplo de eco
- Complementos DE DSP, método DoProcessOutput de ejemplo de eco
- Ejemplo de complemento DSP de eco, método DoProcessOutput
- Ejemplo de complemento DSP de eco, creación del efecto de eco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcb79b5be53f391854f38ce9aeba1c1bbff61ed2c0a982395c7063ff53146760
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902295"
---
# <a name="creating-the-echo-effect"></a>Creación del efecto de eco

Primero debe quitar el código del ejemplo del asistente que escala el audio. En la sección de 8 bits, quite el código siguiente:


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



(Recuerde que m \_ fScaleFactor se ha reemplazado por m \_ dwDelayTime).

En la sección de 16 bits, quite el código siguiente:


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



La implementación de **DoProcessOutput** proporcionada por el código de ejemplo del asistente para complementos crea un bucle while que recorre en iteración una vez por cada ejemplo en el búfer de entrada proporcionado por Reproductor de Windows Media. Este bucle funciona de la misma manera para audio de 8 y 16 bits, aunque se requiere un bucle independiente para cada uno. En cada caso, el bucle se inicia con la siguiente prueba:


```C++
while (dwSamplesToProcess--)

```



Una vez dentro del bucle, las rutinas de procesamiento son muy similares para el audio de 8 y 16 bits. La principal diferencia es que el código de la sección de 8 bits cambia el intervalo de valores de datos a -128 a 127 y, a continuación, vuelve a convertir el intervalo antes de escribir los datos en el búfer de salida. Esto es importante para conservar la simetría de la forma de onda del audio durante el procesamiento.

Ahora puede empezar a agregar y reemplazar código en el bucle de procesamiento.

## <a name="retrieve-a-sample-from-the-input-buffer"></a>Recuperar un ejemplo del búfer de entrada

Durante cada iteración del bucle, se recupera un único ejemplo del búfer de entrada. En el caso del audio de 8 bits, el ejemplo se desplaza al nuevo intervalo y, a continuación, el puntero al búfer de entrada se avanza al ejemplo siguiente. El código siguiente es del asistente para complementos:


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



Para el audio de 16 bits, el proceso es el mismo, excepto para la normalización:


```C++
// Get the input sample.
int i = *pwInputData++;

```



Recuerde que los punteros del código de 16 bits se han convertido al tipo **short**.

## <a name="retrieve-a-sample-from-the-delay-buffer"></a>Recuperación de un ejemplo del búfer de retraso

A continuación, recupere una muestra única del búfer de retraso. Para el código de 8 bits, los ejemplos de retraso se almacenan en su intervalo nativo de 0 a 255. El código siguiente, que debe agregar, recupera un ejemplo de retraso de 8 bits:


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



Para el audio de 16 bits, el proceso es similar:


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a>Escribir el ejemplo de entrada en el búfer de retraso

Ahora, debe almacenar el ejemplo de entrada en el búfer de retraso en la misma ubicación desde la que recuperó la muestra de retraso. A continuación se muestra el código que debe agregar para el audio de 8 bits:


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



Este es el código que se va a agregar para la sección de 16 bits:


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a>Mover el puntero de búfer de retraso

Ahora que el trabajo en el búfer de retraso ha finalizado para esta iteración, puede avanzar el puntero móvil al búfer de retraso. Si el puntero alcanza el final del búfer circular, debe cambiar su valor para que apunte al extremo del búfer. Para ello para audio de 8 bits, use el código siguiente:


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



Este es el código de la sección de 16 bits:


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



Dado que el puntero de la sección de 16 bits es realmente una copia de la variable miembro, debe recordar actualizar el valor de la variable miembro con la nueva dirección. Si no lo hace, el puntero de búfer de retraso apuntará repetidamente al jefe del búfer y el efecto de eco no funcionará según lo previsto. Agregue el código siguiente a la sección de 16 bits:


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a>Mezclar el ejemplo de entrada con el ejemplo de retraso

Aquí es donde se usan los valores de mezcla y mezcla sin mezcla para crear el ejemplo de salida final. Basta con multiplicar cada muestra por el valor de punto flotante que representa el porcentaje de la señal final de la muestra. Multiplique la muestra de entrada por el valor almacenado en m fDryMix; multiplique la muestra de retraso por el valor almacenado \_ en m \_ fWetMix. A continuación, agregue los dos valores. El código que debe agregar es idéntico para las secciones de 8 y 16 bits:


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a>Escribir los datos en el búfer de salida

Por último, copie el ejemplo mixto en el búfer de salida y, a continuación, avance el puntero del búfer de salida. En el caso del audio de 8 bits, el asistente para complementos usa el código siguiente para devolver el ejemplo a su intervalo original:


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



En el caso del audio de 16 bits, el asistente usa el código siguiente como último paso del bucle de procesamiento:


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




