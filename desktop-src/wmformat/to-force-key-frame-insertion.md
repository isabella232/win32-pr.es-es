---
title: Para forzar la inserción de Key-Frame
description: Para forzar la inserción de Key-Frame
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Advanced Systems Format (ASF), forzar inserciones de fotogramas clave
- ASF (formato de sistemas avanzados), forzar inserciones de fotogramas clave
- Advanced Systems Format (ASF), inserciones de fotogramas clave
- ASF (formato de sistemas avanzados), inserciones de fotogramas clave
- fotogramas clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23006eef1e51d8bc63f2d55cac22e09a2052d83e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104487358"
---
# <a name="to-force-key-frame-insertion"></a>Para forzar la inserción de Key-Frame

El códec Windows Media Video 9 admite la inserción de fotogramas clave forzada. Al pasar un ejemplo al escritor, puede especificar que se debe codificar como un [*fotograma clave*](wmformat-glossary.md).

Para forzar la inserción de fotogramas clave para un ejemplo, realice los pasos siguientes.

1.  Asigne un búfer para contener el ejemplo y recupere un puntero a la interfaz [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) que contiene el búfer mediante una llamada a [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Recupere la ubicación y el tamaño del búfer creado en el paso 1 mediante una llamada a [**INSSBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).
3.  Copie los datos de ejemplo en la ubicación del búfer, asegurándose de que el ejemplo que se ha pasado quepa en el búfer asignado. Dependiendo del origen de los ejemplos, puede usar diversas funciones para copiar los datos. Por ejemplo, si va a copiar una secuencia desde un archivo AVI, puede usar la función AVI, **AVIStreamRead**.
4.  Actualice la cantidad de datos que se usan en el búfer para reflejar el tamaño real del ejemplo llamando a [**INSSBuffer:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Obtenga un puntero a la interfaz [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) llamando a **INSSBuffer:: QueryInterface**.
6.  Establezca el ejemplo como un fotograma clave forzado llamando al método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para establecer la \_ propiedad WM SampleExtensionGUID \_ OutputCleanPoint. Esta propiedad es un valor booleano; establézcalo en **true**.
7.  Pase la interfaz de búfer al escritor junto con el número de entrada y el tiempo de muestra mediante el método [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[**Para escribir ejemplos**](to-write-samples.md)
</dt> <dt>

[**Codificación de velocidad de bits variable (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




