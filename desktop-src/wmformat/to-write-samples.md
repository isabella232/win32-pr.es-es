---
title: Para escribir ejemplos
description: Para escribir ejemplos
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- Advanced Systems Format (ASF), escribir ejemplos
- ASF (formato de sistemas avanzados), escribir ejemplos
- Advanced Systems Format (ASF), pasar ejemplos al escritor
- ASF (formato de sistemas avanzados), pasar ejemplos al escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738014b3c42441e878105d12a8ebf23ce4b266f7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420255"
---
# <a name="to-write-samples"></a>Para escribir ejemplos

Cuando haya identificado y configurado las entradas para el archivo que está escribiendo, puede empezar a pasar ejemplos al escritor. Debe pasar los ejemplos en el orden en tiempo de presentación, si es posible, para que el proceso de escritura sea más eficaz.

Antes de pasar cualquier ejemplo, debe establecer el escritor para aceptarlo llamando a [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Para pasar un ejemplo al escritor, realice los pasos siguientes:

1.  Asigne un búfer y recupere un puntero a la interfaz [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) llamando a [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Recupere la dirección del búfer creado en el paso 1 mediante una llamada a [**INSSBuffer:: getBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).
3.  Copie los datos de ejemplo en la ubicación del búfer, asegurándose de que el ejemplo que se ha pasado quepa en el búfer asignado. Puede usar cualquier función de copia de memoria para copiar los datos. Una opción común es memcpy, que se incluye en la biblioteca estándar de tiempo de ejecución de C.
4.  Actualice la cantidad de datos que se usan en el búfer para reflejar el tamaño real del ejemplo llamando a [**INSSBuffer:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Pase la interfaz de búfer al escritor junto con el número de entrada y el tiempo de muestra mediante el método [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) . Todos los ejemplos de audio de una entrada representan la misma duración del contenido, de modo que puede indicar el tiempo de muestra agregando la duración de ejemplo a un total acumulado. En el caso de vídeo, debe calcular el tiempo en función de la velocidad de fotogramas.

**WriteSample** funciona de forma asincrónica y puede que no termine de escribir los datos del búfer antes de que la aplicación esté lista para volver a llamar al método. Por lo tanto, es importante llamar a **AllocateSample** una vez para cada llamada a **WriteSample**. Sin embargo, puede liberar la interfaz **INSSBuffer** inmediatamente después de llamar a **WriteSample**.

Cuando haya terminado de pasar los ejemplos, llame a [**IWMWriter:: EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).

**Nota:** Es importante que los ejemplos de todas las secuencias del archivo se pasen al escritor en la sincronización entre sí. Es decir, siempre que sea posible, debe pasar ejemplos al escritor en el orden en tiempo de presentación dentro de la tolerancia de sincronización especificada en [**IWMWriterAdvanced:: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance). Los mejores resultados se logran cuando los datos se entregan a cada flujo en unidades de un segundo o menos.

Las secuencias también deben terminar aproximadamente al mismo tiempo. Por ejemplo, no debe escribir un archivo con una secuencia de audio de 45 segundos de duración y un flujo de vídeo de 50 segundos de duración. Si codifica este tipo de archivo con entradas sin modificar, algunos de los datos de audio al final de la secuencia se quitarán (aunque sea la secuencia más corta). Para que el trabajo de codificación de archivos funcione, debe agregar 5 segundos de silencio a la entrada de audio para que una secuencia no finalice varios segundos antes que otra. No es necesario que los tipos de secuencia con ejemplos intermitentes, como secuencias de texto o de imagen, se rellenen de esta manera. Las secuencias de comandos de script también deben seguir todas estas reglas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Interfaz IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




