---
title: Para forzar la Key-Frame inserción
description: Para forzar la Key-Frame inserción
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Formato de sistemas avanzados (ASF), forzar inserciones de fotogramas clave
- ASF (formato de sistemas avanzados), forzar inserciones de fotogramas clave
- Formato de sistemas avanzados (ASF), inserciones de fotogramas clave
- ASF (formato de sistemas avanzados), inserciones de fotogramas clave
- fotogramas clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d400c0ee4ba97aa7de559b1394dbe5c9fb2a974c124924aeae0839b1b4dae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196501"
---
# <a name="to-force-key-frame-insertion"></a>Para forzar la Key-Frame inserción

El códec Windows Media Video 9 admite la inserción forzada de fotogramas clave. Al pasar un ejemplo al sistema de escritura, puede especificar que se debe codificar como un [*fotograma clave.*](wmformat-glossary.md)

Para forzar la inserción de fotogramas clave para un ejemplo, realice los pasos siguientes.

1.  Asigne un búfer para contener el ejemplo y recupere un puntero a la interfaz [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) que contiene el búfer mediante una llamada a [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Recupere la ubicación y el tamaño del búfer creado en el paso 1 llamando a [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).
3.  Copie los datos de ejemplo en la ubicación del búfer y asegúrese de que la muestra pasada se ajuste al búfer asignado. Dependiendo del origen de los ejemplos, puede usar diversas funciones para copiar los datos. Por ejemplo, si va a copiar una secuencia desde un archivo AVI, puede usar la función AVI, **AVIStreamRead**.
4.  Actualice la cantidad de datos usados en el búfer para reflejar el tamaño real del ejemplo mediante una llamada a [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Obtenga un puntero a la [**interfaz INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) llamando a **INSSBuffer::QueryInterface**.
6.  Establezca el ejemplo como un fotograma clave forzado llamando al método [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para establecer la propiedad \_ SampleExtensionGUID \_ OutputCleanPoint de WM. Esta propiedad es un valor booleano; estadíla en **TRUE.**
7.  Pase la interfaz de búfer al escritor junto con el número de entrada y la hora de ejemplo mediante el [**método IWMWriter::WriteSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[**Para escribir ejemplos**](to-write-samples.md)
</dt> <dt>

[**Codificación de velocidad de bits variable (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




