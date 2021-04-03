---
title: Crear el efecto de eco
description: Crear el efecto de eco
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Complementos de Media Player de Windows, método echo de ejemplo DoProcessOutput
- complementos, método echo de ejemplo DoProcessOutput
- Complementos de procesamiento de señal digital, ejemplo echo método DoProcessOutput
- Complementos DSP, método echo de ejemplo DoProcessOutput
- Ejemplo de complemento DSP de eco, método DoProcessOutput
- Ejemplo de complemento DSP de eco, creación de efecto de eco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075160"
---
# <a name="creating-the-echo-effect"></a>Crear el efecto de eco

Primero debe quitar el código del ejemplo de asistente que escala el audio. En la sección de 8 bits, quite el código siguiente:


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



La implementación de **DoProcessOutput** proporcionada por el código de ejemplo del Asistente para complementos crea un bucle while que recorre en iteración una vez cada muestra en el búfer de entrada proporcionado por Windows Media Player. Este bucle funciona de la misma manera para audio de 8 y 16 bits, aunque se requiere un bucle independiente para cada uno. En cada caso, el bucle se inicia con la prueba siguiente:


```C++
while (dwSamplesToProcess--)

```



Una vez dentro del bucle, las rutinas de procesamiento son muy similares para audio de 8 y 16 bits. La principal diferencia es que el código de la sección de 8 bits cambia el intervalo de valores de datos a-128 a 127 y, a continuación, vuelve a convertir el intervalo antes de escribir los datos en el búfer de salida. Esto es importante para conservar la simetría de la forma de onda de audio durante el procesamiento.

Ahora puede empezar a agregar y reemplazar código en el bucle de procesamiento.

## <a name="retrieve-a-sample-from-the-input-buffer"></a>Recuperación de un ejemplo desde el búfer de entrada

Durante cada iteración del bucle, se recupera un solo ejemplo del búfer de entrada. En el caso de audio de 8 bits, el ejemplo se desplaza al nuevo intervalo y, a continuación, el puntero al búfer de entrada está avanzado en el ejemplo siguiente. El código siguiente procede del Asistente para complementos:


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



En el caso de audio de 16 bits, el proceso es el mismo, salvo por la normalización:


```C++
// Get the input sample.
int i = *pwInputData++;

```



Recuerde que los punteros en el código de 16 bits se han convertido al tipo **Short**.

## <a name="retrieve-a-sample-from-the-delay-buffer"></a>Recuperación de un ejemplo del búfer de retraso

A continuación, recupere un solo ejemplo del búfer de retraso. En el caso de código de 8 bits, las muestras de retraso se almacenan en su intervalo nativo de 0 a 255. El código siguiente, que debe agregar, recupera un ejemplo de retraso de 8 bits:


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



En el caso de audio de 16 bits, el proceso es similar:


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a>Escribir el ejemplo de entrada en el búfer de retraso

Ahora, debe almacenar el ejemplo de entrada en el búfer de retraso en la misma ubicación desde la que recuperó el ejemplo de retraso. El siguiente es el código que debe agregar para el audio de 8 bits:


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



Este es el código que se va a agregar para la sección de 16 bits:


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a>Desplace el puntero de búfer de retraso

Ahora que ha finalizado el trabajo en el búfer de retraso para esta iteración, puede avanzar el puntero movible al búfer de retraso. Si el puntero alcanza el final del búfer circular, debe cambiar su valor para que apunte al encabezado del búfer. Para hacer esto para el audio de 8 bits, use el código siguiente:


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



Puesto que el puntero de la sección de 16 bits es realmente una copia de la variable miembro, debe recordar actualizar el valor de la variable miembro con la nueva dirección. Si no lo hace, el puntero de búfer de retraso apuntará repetidamente al encabezado del búfer y el efecto de eco no funcionará según lo esperado. Agregue el código siguiente a la sección de 16 bits:


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a>Mezclar el ejemplo de entrada con el ejemplo de retraso

Aquí es donde se usan los valores de mezcla húmeda y mezcla seca para crear el ejemplo de salida final. Basta con multiplicar cada ejemplo por el valor de punto flotante que representa el porcentaje de la señal final para el ejemplo. Multiplique el ejemplo de entrada por el valor almacenado en m \_ fDryMix; multiplique el ejemplo de retraso por el valor almacenado en m \_ fWetMix. A continuación, agregue los dos valores. El código que debe agregar es idéntico para las secciones de 8 y 16 bits:


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a>Escribir los datos en el búfer de salida

Por último, copie la muestra mixta en el búfer de salida y, a continuación, avance el puntero del búfer de salida. En el caso de audio de 8 bits, el Asistente para complementos usa el código siguiente para devolver el ejemplo a su intervalo original:


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



En el caso de audio de 16 bits, el asistente usa el siguiente código como último paso del bucle de procesamiento:


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




