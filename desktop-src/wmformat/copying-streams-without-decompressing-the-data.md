---
title: Copiar secuencias sin descomprimir los datos
description: Copiar secuencias sin descomprimir los datos
ms.assetid: c268ce44-a09d-4304-bc39-8b6657da2bdb
keywords:
- SDK de Windows Media Format, copiar flujos
- Advanced Systems Format (ASF), copiar flujos
- ASF (formato de sistemas avanzados), copiar flujos
- secuencias, copiar sin descomprimir datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831b85ad431a6c4d3f4255c281d22ca17004674f
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "104420436"
---
# <a name="copying-streams-without-decompressing-the-data"></a>Copiar secuencias sin descomprimir los datos

La forma más sencilla y común de copiar una secuencia de un archivo a otro consiste en recuperar los ejemplos en su estado comprimido y, después, escribirlos en el nuevo archivo sin descomprimirlos y volver a comprimirlos. Los ejemplos obtenidos de un archivo en su estado comprimido se denominan ejemplos de secuencias, porque no se modifican de su representación en la secuencia. Se recomienda usar siempre ejemplos de secuencias para copiar flujos, ya que descomprimir y volver a comprimir los datos multimedia digitales degrada la calidad. Si debe copiar un flujo de datos descomprimidos, vea [copiar transmisiones mediante ejemplos descomprimidos](copying-streams-using-decompressed-samples.md).

Es posible concatenar dos o más secuencias en un único flujo mediante ejemplos comprimidos, pero solo si las velocidades de bits son idénticas. El proceso es esencialmente el mismo que los pasos descritos a continuación, salvo que debe leer varios archivos originales para obtener todo el contenido que necesita. Sin embargo, solo puede escribir ejemplos comprimidos de varios archivos en una única secuencia si las estructuras de **\_ \_ tipo de medio de WM** (incluidos todos los miembros de la estructura **pbFormat** ) de todas las secuencias comprimidas son idénticas. Para combinar datos de varias secuencias que no tienen el mismo formato, debe descomprimir el contenido y volver a comprimirlo en el flujo de destino. Además, al combinar datos de dos o más flujos en un solo flujo, debe agregar los valores de la ventana de búfer para todas las secuencias de forma conjunta para obtener la ventana de búfer de la nueva secuencia. Esto se debe a que no es posible determinar qué parte del búfer se toma al final de una secuencia y al principio de otra.

Puede recuperar ejemplos de secuencias con el lector asincrónico mediante [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples). Los ejemplos de secuencias se entregan a [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample), no a [**IWMReaderCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Si está leyendo un archivo y recuperando algunos flujos comprimidos y algunos descomprimidos, debe implementar ambos métodos de devolución de llamada.

El lector sincrónico proporciona más flexibilidad para recuperar ejemplos. Puede cambiar entre los ejemplos comprimidos y descomprimidos libremente durante la reproducción mediante [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples).

Para copiar una secuencia completa de un archivo ASF a un nuevo archivo ASF, realice los pasos siguientes. En estos pasos se usa el lector sincrónico porque es mucho más fácil de usar para este tipo de operación.

1.  Cree un objeto de lector sincrónico llamando a la función [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) .
2.  Abra un archivo en el lector con una llamada a [**IWMSyncReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).
3.  Obtiene un puntero a la interfaz [**IWMProfile**](iwmprofile.md) del objeto lector sincrónico llamando a **IWMSyncReader:: QueryInterface**.
4.  Recupere las propiedades de la secuencia deseada llamando a [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber). Se recuperará un puntero a la interfaz [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) del objeto de configuración de secuencia para la secuencia que desee.
5.  Obtiene una copia de la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para la secuencia. Realice dos llamadas a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype): la primera para obtener el tamaño de la estructura, la segunda para obtener la propia estructura.
6.  Cree un objeto de administrador de perfiles mediante una llamada a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
7.  Llame a [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) para crear un nuevo perfil (o abra un perfil existente al que desee agregar el flujo). Llame a [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) en el nuevo perfil para agregar la secuencia del archivo existente. Al agregar la secuencia, use el puntero **IWMStreamConfig** obtenido en el paso 4.
8.  Cree un objeto de escritor con una llamada a la función [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . Establezca el perfil que se acaba de crear como el perfil activo en el escritor mediante una llamada a [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). Cree un archivo para la salida mediante una llamada a [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).
9.  Para cada entrada asociada a la secuencia o flujos que está copiando, llame a [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops), pasando **null** para la interfaz [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) . Esto informa al objeto del escritor de que no necesita validar los datos que está pasando. Debe realizar esta llamada antes de llamar a **BeginWriting** (paso 14); de lo contrario, es posible que un objeto de lectura no pueda descodificar el contenido.
10. Establezca el lector sincrónico para proporcionar ejemplos de secuencias comprimidas para la secuencia seleccionada llamando a [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) con el parámetro *FCompressed* establecido en true.
11. Obtenga información del códec para cada flujo que se va a copiar y agregue la información del códec al encabezado antes de la escritura. Para obtener la información del códec, llame a [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) y [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar los códecs asociados al archivo en el lector. Seleccione la información del códec que coincida con la configuración de la secuencia. A continuación, establezca la información del códec en el escritor llamando a [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), pasando la información obtenida del lector.
12. Obtenga un puntero a la interfaz [**IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced) llamando a **IWMWriter:: QueryInterface**.
13. Establezca el escritor en el modo de escritura mediante una llamada a [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).
14. Realice llamadas repetidas a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample), especificando el número de flujo deseado. Cuando se reciban los ejemplos, páselo al escritor mediante llamadas a [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample). En el caso de las secuencias de vídeo, debe comprobar las marcas (si existen) establecidas por el escritor en cada llamada a **GetNextSample**. Si \_ \_ se establece WM SF CLEANPOINT, también debe establecerla en la llamada a **WriteStreamSample**.
15. Cuando se complete la lectura, llame a [**IWMWriter:: EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting). La secuencia se debe transferir.

> [!Note]  
> Los flujos de imagen no se pueden copiar de un archivo a otro mediante ejemplos de secuencias. Para copiar los datos del flujo de imagen, recupere los ejemplos sin comprimir y, a continuación, procese a través del escritor como lo haría normalmente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Copiar datos de un archivo a otro**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copiar secuencias mediante ejemplos descomprimidos**](copying-streams-using-decompressed-samples.md)
</dt> </dl>

 

 




