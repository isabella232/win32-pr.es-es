---
title: Implementación de IMediaObject AllocateStreamingResources
description: Implementación de IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Complementos de Windows Media Player, echo ejemplo de recursos de streaming
- complementos, echo ejemplo de recursos de streaming
- Complementos de procesamiento de señal digital, echo ejemplo de recursos de streaming
- Complementos DSP, echo ejemplo de recursos de streaming
- Ejemplo de complemento DSP de eco, recursos de streaming
- Ejemplo de complemento DSP de eco, búfer de retraso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e347e35eaabbcbcc00a586e4cba0d8ad31cc6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418831"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a>Implementación de IMediaObject:: AllocateStreamingResources

En el ejemplo echo, el método **AllocateStreamingResources** crea el búfer de retraso. Para ello, hace lo siguiente:

1.  Calcular un tamaño para el búfer que corresponde al tiempo de retraso especificado para el tipo de medio especificado.
2.  Asignando nueva memoria o reasignando el tamaño del búfer si ya existe.
3.  Llamar a un método que rellena el búfer con valores que representan el silencio.

El valor del silencio es diferente en función de la profundidad de bits. En el caso de audio de 8 bits, el silencio se representa mediante el valor hexadecimal 80; en el caso de audio de 16 bits, el silencio se representa con cero.

## <a name="calculating-the-delay-buffer-size"></a>Calcular el tamaño del búfer de retraso

Para calcular el tamaño necesario para el búfer de retraso, primero debe recuperar una estructura **WAVEFORMATEX** que contenga información sobre los datos de audio. En el ejemplo siguiente se recupera un puntero a esta estructura a partir de la estructura de **\_ \_ tipo de medio DMO** de entrada:


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



Una vez que haya almacenado un puntero a la estructura **WAVEFORMATEX** adecuada, puede inspeccionar sus miembros y usarlos para calcular el tamaño de búfer necesario. En el ejemplo de código siguiente se muestra esto:


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



Este algoritmo calcula el tamaño del búfer multiplicando el tiempo de retraso, en milisegundos, por el número de muestras por milisegundo, multiplicando el resultado por el número de canales y multiplicando el resultado por el número de bytes por muestra. El número de canales y el número de bytes por muestra no son obvios; se codifican en el miembro nBlockAlign. La división por 1000 reduce el valor de nSamplesPerSec a muestras por milisegundo; el milisegundo es la unidad deseada porque el tiempo de retardo se expresa en milisegundos.

## <a name="allocating-the-delay-buffer-memory"></a>Asignación de memoria de búfer de retraso

Una vez que haya calculado los requisitos de memoria, puede asignar el búfer. Es posible que sea necesario eliminar el búfer si existe, como cuando el usuario invoca la página de propiedades para cambiar el valor de tiempo de retraso. En el código siguiente se muestra la asignación del búfer de retraso:


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



Si el búfer se asigna correctamente, debe mover el puntero movible al encabezado del búfer, tal y como se muestra en el ejemplo siguiente:


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a>Llenado del búfer de retraso con silencio

Es conveniente escribir un método para rellenar el búfer de retraso con valores que representan el silencio. El método debe recibir el puntero a la estructura WAVEFORMATEX válida y, a continuación, inspeccionar el miembro wBitsPerSample para determinar si el audio es de 8 bits o superior. En el ejemplo siguiente se rellena el búfer de retraso con el valor correcto para el silencio:


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



No olvide agregar la declaración adelantada de la función al archivo de encabezado echo. h en la sección privada:


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



Debe agregar código al final de AllocateStreamingResources para llamar a este método cada vez que se crea o se cambia el tamaño del búfer de retraso. En el código de ejemplo siguiente se pasa el puntero WAVEFORMATEX denominado pWave al nuevo método:


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a>Reasignar la memoria del búfer de retraso

Cuando el usuario cambia el tiempo de retraso mediante la página de propiedades, el tamaño del búfer de retraso también debe cambiar. Ya ha agregado el código a AllocateStreamingResources para cambiar el tamaño del búfer, pero debe agregar una línea de código a CEcho::p \_ retraso de UT para llamar al método de asignación de recursos cada vez que cambie el valor de la propiedad. Este es el código:


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con recursos de streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




