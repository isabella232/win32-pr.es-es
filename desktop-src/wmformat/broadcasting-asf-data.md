---
title: Difusión de datos de ASF
description: Difusión de datos de ASF
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows SDK de formato multimedia, difusión de datos de ASF
- Formato de sistemas avanzados (ASF), difusión de datos
- ASF (formato de sistemas avanzados), difusión de datos
- Windows SDK de formato multimedia, envío de datos de ASF
- Formato de sistemas avanzados (ASF), envío de datos
- ASF (formato de sistemas avanzados), enviar datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44fc9ea0515822c765b0cb3af457254341a64f08e64d566aa9e226a48758e7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434469"
---
# <a name="broadcasting-asf-data"></a>Difusión de datos de ASF

En este tema se describe cómo enviar datos de ASF a través de una red mediante el protocolo HTTP. El envío de archivos a través de una red requiere el uso del objeto de escritor, por lo que debe tener un conocimiento general de este objeto antes de leer este tema. Para obtener más información, vea [Escribir archivos ASF.](writing-asf-files.md)

Si empieza con datos sin comprimir, haga lo siguiente:

1.  Cree el objeto de escritor llamando a [**la función WMCreateWriter.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) Esta función devuelve un **puntero IWMWriter.**
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  Cree el objeto de receptor de red llamando a la [**función WMCreateWriterNetworkSink,**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) que devuelve un **puntero IWMWriterNetworkSink.**
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  Llame [**a IWMWriterNetworkSink::Open en**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) el receptor de red y especifique el número de puerto que se debe abrir; por ejemplo, 8080. Opcionalmente, llame [**a IWMWriterNetworkSink::GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) para obtener la dirección URL del host. Los clientes accederán al contenido desde esta dirección URL. También puede llamar a [**IWMWriterNetworkSink::SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) para restringir el número de clientes.
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  Asocie el receptor de red al escritor mediante una llamada a [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) en el escritor, con un puntero a la interfaz **IWMWriterNetworkSink** del receptor de red.
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  Establezca el perfil de ASF llamando al método [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) en el objeto writer, con un [**puntero IWMProfile.**](iwmprofile.md) Para obtener información sobre cómo crear un perfil, vea [Trabajar con perfiles](working-with-profiles.md).
6.  Opcionalmente, especifique los metadatos mediante la [**interfaz IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) en el escritor.
7.  Llame [**a IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) en el sistema de escritura.
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  Para cada ejemplo, llame al [**método IWMWriter::WriteSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) Especifique el número de secuencia, el tiempo de presentación, la duración del ejemplo y un puntero al búfer de ejemplo. El **método WriteSample** comprime los ejemplos.
9.  Cuando haya terminado, llame a [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) en el sistema de escritura.
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. Llame [**a IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) en el escritor para desasociar el objeto receptor de red.
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. Llame [**a IWMWriterNetworkSink::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) en el receptor de red para liberar el puerto.
    ```C++
    hr = pNetSink->Close();
    ```

    

Otra manera de transmitir contenido de ASF a través de una red es leerlo desde un archivo ASF existente. El ejemplo WMVNetWrite proporcionado en el SDK muestra este enfoque. Además de los pasos enumerados anteriormente, haga lo siguiente:

1.  Cree un objeto de lector y llame al **método Open** con el nombre del archivo.
2.  Llame [**a IWMReaderAdvanced::SetManualStreamSelection en**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) el objeto reader, con el valor **TRUE**. Esto permite que la aplicación lea todas las secuencias del archivo, incluidas las secuencias con exclusión mutua.
3.  Consulte el lector para la [**interfaz IWMProfile.**](iwmprofile.md) Use este puntero cuando llame a [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) en el objeto writer (paso 5 del procedimiento anterior).
4.  Para cada secuencia definida en el perfil, llame a [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) para obtener el número de secuencia. Pase este número de secuencia al método [**IWMReaderAdvanced::SetReceiveStreamSamples del**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) lector. Este método informa al lector para que entregue muestras comprimidas, en lugar de decodificarlos. Los ejemplos se entregarán a la aplicación a través del método de devolución de llamada [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) de la aplicación.

    Debe obtener información de códec para cada secuencia que lea sin comprimir y agregarla al encabezado antes de la difusión. Para obtener la información del códec, llame a [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar los códecs asociados al archivo en el lector. Seleccione la información del códec que coincida con la configuración del flujo. A continuación, establezca la información del códec en el escritor mediante una llamada [**a IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), pasando la información obtenida del lector.

5.  Después de establecer el perfil en el escritor, llame a [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) en el escritor para obtener el número de entradas. Para cada entrada, llame [**a IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) con el valor **NULL**. Esto indica al objeto de escritor que la aplicación entregará muestras comprimidas, por lo que el escritor no tiene que usar códecs para comprimir los datos. Asegúrese de llamar a **SetInputProps antes** de llamar **a BeginWriting**.
6.  Opcionalmente, copie los atributos de metadatos del lector al escritor.
7.  Dado que los ejemplos del lector ya están comprimidos, use el método [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) para escribir los ejemplos, en lugar del **método WriteSample.** El **método WriteStreamSample** omite los procedimientos de compresión habituales del objeto de escritura.
8.  Cuando el lector llega al final del archivo, envía una notificación \_ WMT EOF a la aplicación.

Además, la aplicación debe impulsar el reloj en el objeto de lector, de modo que el lector extraiga los datos del archivo lo antes posible. Para ello, llame al método [**IWMReaderAdvanced::SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) en el lector, con el **valor TRUE**. Después de que el lector envíe la notificación WMT STARTED, llame a \_ [**IWMReaderAdvanced::D eliverTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) y especifique el intervalo de tiempo que el lector debe entregar. Una vez que el lector haya terminado de leer este intervalo de tiempo, llama al método de devolución de llamada [**IWMReaderCallbackAdvanced::OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) de la aplicación. La aplicación debe llamar de **nuevo a DeliverTime** para leer el siguiente intervalo de tiempo. Por ejemplo, para leer del archivo en intervalos de un segundo:


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Envío de datos de ASF a través de una red**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




