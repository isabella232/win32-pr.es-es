---
title: Para escribir ejemplos
description: Para escribir ejemplos
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- Formato de sistemas avanzados (ASF), escribir ejemplos
- ASF (formato de sistemas avanzados), escribir ejemplos
- Formato de sistemas avanzados (ASF), pasar ejemplos al escritor
- ASF (formato de sistemas avanzados), pasar ejemplos al escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738014b3c42441e878105d12a8ebf23ce4b266f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251438"
---
# <a name="to-write-samples"></a>Para escribir ejemplos

Cuando haya identificado y configurado las entradas para el archivo que está escribiendo, puede empezar a pasar ejemplos al escritor. Debe pasar ejemplos en tiempo de presentación, si es posible, para que el proceso de escritura sea más eficaz.

Antes de pasar cualquier ejemplo, debe establecer el escritor para que los acepte llamando a [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Para pasar un ejemplo al escritor, realice los pasos siguientes:

1.  Asigne un búfer y recupere un puntero a la [**interfaz INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) llamando a [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Recupere la dirección del búfer creado en el paso 1 llamando a [**INSSBuffer::GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).
3.  Copie los datos de ejemplo en la ubicación del búfer y asegúrese de que el ejemplo pasado se ajuste al búfer asignado. Puede usar cualquier función de copia de memoria para copiar los datos. Una opción común es memcpy, que se incluye en la biblioteca en tiempo de ejecución de C estándar.
4.  Actualice la cantidad de datos usados en el búfer para reflejar el tamaño real del ejemplo mediante una llamada a [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Pase la interfaz de búfer al escritor junto con el número de entrada y la hora de ejemplo mediante el [**método IWMWriter::WriteSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) Todas las muestras de audio de una entrada representan la misma duración del contenido, por lo que puede calcular el tiempo de la muestra agregando la duración de la muestra a un total de ejecución. En el caso del vídeo, debe calcular el tiempo en función de la velocidad de fotogramas.

**WriteSample** funciona de forma asincrónica y es posible que no termine de escribir los datos del búfer antes de que la aplicación esté lista para llamar al método de nuevo. Por lo tanto, es importante llamar a **AllocateSample una** vez para cada llamada a **WriteSample**. Sin embargo, puede liberar la **interfaz INSSBuffer** inmediatamente después de llamar a **WriteSample**.

Cuando haya terminado de pasar ejemplos, llame a [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).

**Nota** Es importante que los ejemplos de todas las secuencias del archivo se pasen al escritor en sincronización entre sí. Es decir, siempre que sea posible, debe pasar ejemplos al escritor en el orden de presentación dentro de la tolerancia de sincronización especificada en [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance). Los mejores resultados se logran cuando los datos se entregan a cada secuencia en unidades de un segundo o menos.

Secuencias también debe terminar aproximadamente al mismo tiempo. Por ejemplo, no debe escribir un archivo con una secuencia de audio de 45 segundos y una secuencia de vídeo de 50 segundos. Si codifica este tipo de archivo con entradas sin modificar, algunos de los datos de audio al final de la secuencia se descartarán (aunque sea la secuencia más corta). Para que la codificación de archivos funcione, debe agregar 5 segundos de silencio a la entrada de audio para que una secuencia no finalice varios segundos antes que otra. No es necesario que los tipos de secuencia con muestras intermitentes, como flujos de texto o de imagen, se acoliquen de esta manera. Los flujos de comandos de script también deben seguir todas estas reglas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**IWMWriter (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




