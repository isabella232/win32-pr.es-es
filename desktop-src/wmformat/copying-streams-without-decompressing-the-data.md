---
title: Copiar Secuencias sin descomprimir los datos
description: Copiar Secuencias sin descomprimir los datos
ms.assetid: c268ce44-a09d-4304-bc39-8b6657da2bdb
keywords:
- Windows SDK de formato multimedia, copiar secuencias
- Formato de sistemas avanzados (ASF), copiar secuencias
- ASF (formato de sistemas avanzados), copiar secuencias
- streams,copying without decompressing data
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831b85ad431a6c4d3f4255c281d22ca17004674f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360234"
---
# <a name="copying-streams-without-decompressing-the-data"></a>Copiar Secuencias sin descomprimir los datos

La manera más sencilla y común de copiar una secuencia de un archivo a otro es recuperar los ejemplos en su estado comprimido y, a continuación, escribirlos en el nuevo archivo sin descomprimirlos y volver a comprimirlos. Las muestras obtenidas de un archivo en su estado comprimido se denominan muestras de secuencia, porque no se alteran a partir de su representación en la secuencia. Se recomienda usar siempre ejemplos de secuencias para copiar secuencias, ya que la descompresión y la recompresión de datos multimedia digitales degradan la calidad. Si debe copiar una secuencia de datos descomprimidos, vea Copiar Secuencias [mediante ejemplos descomprimidos.](copying-streams-using-decompressed-samples.md)

Es posible concatenar dos o más secuencias en una sola secuencia mediante muestras comprimidas, pero solo si las velocidades de bits son idénticas. El proceso es esencialmente el mismo que los pasos descritos a continuación, salvo que debe leer varios archivos originales para obtener todo el contenido que necesita. Sin embargo, solo puede escribir ejemplos comprimidos de varios archivos en una sola secuencia si las estructuras **DE TIPO \_ MULTIMEDIA \_ de WM** (incluidos todos los miembros de la estructura **pbFormat)** de todas las secuencias comprimidas son idénticas. Para combinar datos de varios flujos que no tienen el mismo formato, debe descomprimir el contenido y volver acomprimirlo en la secuencia de destino. Además, al combinar datos de dos o más secuencias en una sola secuencia, debe agregar los valores de la ventana de búfer para todas las secuencias juntas para obtener la ventana de búfer para la nueva secuencia. Esto se debe a que es imposible determinar cuánto búfer se toma al final de una secuencia y al principio de otra.

Puede recuperar ejemplos de secuencia con el lector asincrónico mediante [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples). Los ejemplos de secuencia se entregan a [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample), no a [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Si está leyendo un archivo y recuperando algunas secuencias comprimidas y otras descomprimidas, debe implementar ambos métodos de devolución de llamada.

El lector sincrónico proporciona más flexibilidad para recuperar ejemplos. Puede cambiar libremente entre muestras comprimidas y descomprimidas durante la reproducción mediante [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples).

Para copiar una secuencia completa de un archivo ASF a un nuevo archivo ASF, realice los pasos siguientes. En estos pasos se usa el lector sincrónico porque es mucho más fácil de usar para este tipo de operación.

1.  Cree un objeto de lector sincrónico mediante una llamada a [**la función WMCreateSyncReader.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)
2.  Abra un archivo en el lector con una llamada a [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).
3.  Obtenga un puntero a la [**interfaz IWMProfile**](iwmprofile.md) del objeto de lector sincrónico llamando a **IWMSyncReader::QueryInterface**.
4.  Recupere las propiedades de la secuencia deseada llamando a [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber). Esto recuperará un puntero a la [**interfaz IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) del objeto de configuración de flujo para la secuencia que desee.
5.  Obtenga una copia de la estructura [**WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para la secuencia. Realice dos llamadas a [**IWMMediaProps::GetMediaType:**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)la primera para obtener el tamaño de la estructura y la segunda para obtener la propia estructura.
6.  Cree un objeto de administrador de perfiles mediante una llamada a [**la función WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
7.  Llame a [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) para crear un nuevo perfil (o abra un perfil existente al que quiera agregar la secuencia). Llame [**a IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) en el nuevo perfil para agregar la secuencia desde el archivo existente. Al agregar la secuencia, use el **puntero IWMStreamConfig** obtenido en el paso 4.
8.  Cree un objeto de escritor con una llamada a la [**función WMCreateWriter.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) Establezca el perfil recién creado como perfil activo en el sistema de escritura mediante una llamada [**a IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). Cree un archivo para la salida mediante una [**llamada a IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).
9.  Para cada entrada asociada a la secuencia o secuencias que va a copiar, llame a [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops)y pase **NULL** para la [**interfaz IWMInputMediaProps.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) Esto informa al objeto de escritor de que no es necesario validar los datos que se pasan. Debe realizar esta llamada antes de llamar a **BeginWriting** (paso 14), de lo contrario, es posible que un objeto de lectura no pueda descodificar el contenido.
10. Establezca el lector sincrónico para entregar ejemplos de secuencias comprimidas para la secuencia seleccionada mediante una llamada a [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) con el *parámetro fCompressed* establecido en True.
11. Obtenga información de códec para cada secuencia que se va a copiar y agregue la información del códec al encabezado antes de escribir. Para obtener la información del códec, llame a [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar los códecs asociados al archivo en el lector. Seleccione la información del códec que coincida con la configuración del flujo. A continuación, establezca la información del códec en el escritor mediante una llamada [**a IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), pasando la información obtenida del lector.
12. Obtenga un puntero a [**la interfaz IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced) llamando a **IWMWriter::QueryInterface**.
13. Establezca el sistema de escritura en modo de escritura mediante una [**llamada a IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).
14. Realice llamadas repetidas [**a IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample), especificando el número de secuencia deseado. Cuando se reciben ejemplos, páselos al escritor con llamadas a [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample). En el caso de las secuencias de vídeo, debe comprobar las marcas (si las hay) establecidas por el escritor en cada llamada a **GetNextSample**. Si se \_ establece WM SF \_ CLEANPOINT, también debe establecerlo en la llamada a **WriteStreamSample**.
15. Una vez completada la lectura, llame [**a IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting). La secuencia debe transferirse.

> [!Note]  
> Los flujos de imágenes no se pueden copiar de un archivo a otro mediante ejemplos de secuencias. Para copiar datos de flujo de imágenes, recupere los ejemplos sin comprimir y procese a través del sistema de escritura como lo haría normalmente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Copiar datos de un archivo a otro**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copiar Secuencias ejemplos descomprimidos**](copying-streams-using-decompressed-samples.md)
</dt> </dl>

 

 




