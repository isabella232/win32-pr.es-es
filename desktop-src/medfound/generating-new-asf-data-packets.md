---
description: Generación de nuevos paquetes de datos de ASF
ms.assetid: 7afa9694-c965-40e2-8549-e32ff48def2a
title: Generación de nuevos paquetes de datos de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9473037d656bd4fcc01b91a908103fcda3e364a36e8caaf42cfc0558381e5af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742084"
---
# <a name="generating-new-asf-data-packets"></a>Generación de nuevos paquetes de datos de ASF

El *multiplexor* de ASF es un componente de capa WMContainer que funciona con el objeto de datos [ASF](asf-file-structure.md) y ofrece a una aplicación la capacidad de generar paquetes de datos de ASF para una secuencia que cumple los requisitos definidos en el objeto ContentInfo.

El multiplexor tiene una entrada y una salida. Recibe un ejemplo de secuencia que contiene datos multimedia digitales y genera uno o varios paquetes de datos que se pueden escribir en un contenedor de ASF.

En la lista siguiente se resume el proceso de generación de paquetes de datos de ASF:

1.  Pase los datos de entrada al multiplexor [**en IMFASFMultiplexer::P rocessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).
2.  Recopile los paquetes de datos mediante una llamada a [**MULTICASTASFMultiplexer::GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) en un bucle hasta que se hayan recuperado todos los paquetes completos.
3.  Una vez convertidos los datos de entrada en paquetes completos, puede haber algunos datos pendientes en el multiplexor, que [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)no recuperó. Llame [**a IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) para empaquetar los ejemplos pendientes y recopilarlos del multiplexor llamando de nuevo a **GetNextPacket.**
4.  Actualice los objetos de encabezado ASF asociados llamando a [**ALFMULTIPLEXer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) para reflejar los cambios realizados por el multiplexor durante la generación de paquetes de datos.

En el diagrama siguiente se muestra la generación de paquetes de datos para un archivo ASF a través del multiplexor.

![diagrama que muestra la generación de paquetes de datos para un archivo asf](images/packet.gif)

## <a name="asf-data-packet-creation"></a>Creación de paquetes de datos de ASF

Después de crear e inicializar el [multiplexor](creating-the-multiplexer-object.md)tal y como se describe en Creación del objeto multiplexor, llame a [**MULTICASTASFMultiplexer::P rocessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) para pasar datos de entrada al multiplexor para procesarlos en paquetes de datos. La entrada especificada debe estar en un ejemplo multimedia (interfaz [**DE PRUEBASEJEMPLO)**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que puede tener uno o varios búferes multimedia (interfaz [**DENMEDIABuffer)**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) que contengan los datos de una secuencia. En el caso de la transcodificación de ASF a ASF, el ejemplo de medios de entrada se puede generar a partir del divisor que crea ejemplos de flujos en paquetes. Para obtener más información, [vea ASF Splitter](asf-splitter.md).

Antes de llamar [**a ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), asegúrese de que la marca de tiempo del ejemplo de medios de entrada es un tiempo de presentación válido; De lo **contrario, ProcessSample** produce un error y devuelve el código MF \_ E NO SAMPLE \_ \_ \_ TIMESTAMP.

El multiplexor puede aceptar la entrada como ejemplos de medios comprimidos o sin comprimir a través [**de ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample). El multiplexor asigna tiempos de envío a estos ejemplos en función del uso de ancho de banda de la secuencia. Durante este proceso, el multiplexor comprueba los parámetros del cubo de fugas (velocidad de bits y uso de la ventana de búfer) y puede rechazar muestras que no cumplan esos valores. El ejemplo de medios de entrada puede producir un error en la comprobación de ancho de banda por cualquiera de los siguientes motivos:

-   Si el ejemplo de medios de entrada llegó tarde porque la hora de envío asignada por última vez es mayor que la marca de tiempo en este ejemplo multimedia. [**ProcessSample produce un**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) error y devuelve el código de error **MF E LATE \_ \_ \_ SAMPLE.**
-   Si la marca de tiempo en el ejemplo de medios de entrada es anterior a la hora de envío asignada (esto indica desbordamiento del búfer). El multiplexor puede omitir esta situación si está configurado para ajustar la velocidad de bits estableciendo la marca **MFASF \_ \_ MULTIPLEXER AUTOADJUST \_ BITRATE** durante la inicialización del multiplexor. Para obtener más información, vea "Multiplexer Initialization and Leaky Bucket Configuración" (Inicialización de multiplexador y pérdida de Configuración) en Creating the Multiplexer Object (Creación [del objeto multiplexador).](creating-the-multiplexer-object.md) Si no se establece esta marca y el multiplexor encuentra saturación de ancho de banda, [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) produce un error y devuelve el código de error **MF E BANDWIDTH \_ \_ \_ OVERRUN.**

Una vez que el multiplexor asigna el tiempo de envío, el ejemplo de medios de entrada se agrega a la ventana de envío, una lista de ejemplos de medios de entrada ordenados por tiempos de envío y listos para procesarse en paquetes de datos. Durante la construcción de paquetes de datos, se analiza el ejemplo de medios de entrada y los datos pertinentes se escriben en un paquete de datos como carga. Un paquete de datos completo puede contener datos de uno o varios ejemplos de medios de entrada.

Cuando llegan nuevos ejemplos de medios de entrada a la ventana de envío, se agregan a una cola hasta que haya suficientes ejemplos multimedia para formar un paquete completo. Los datos de los búferes multimedia contenidos en el ejemplo de medios de entrada no se copian en el paquete de datos generado. El paquete de datos contiene referencias a los búferes multimedia de entrada hasta que el ejemplo de medios de entrada se ha paqueteado completamente y se ha recopilado el paquete completo del multiplexor.

Cuando hay disponible un paquete de datos completo, se puede recuperar mediante una llamada a [**IMFASFMultiplexer::GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket). Si llama a [**ProcessSample mientras**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) hay paquetes completos listos para la recuperación, se produce un error y devuelve el código de error **MF E \_ \_ NOTACCEPTING.** Esto indica que el multiplexor no puede aceptar más entradas y debe llamar a **GetNextPacket para** recuperar los paquetes en espera. Idealmente, cada **llamada a ProcessSample** debe ir seguida de una o varias llamadas **GetNextPacket** para obtener los paquetes de datos completos. Puede tardar más de un ejemplo de medios de entrada para crear un paquete de datos completo. Por el contrario, los datos de una muestra de medios de entrada pueden abarcar varios paquetes. Por lo tanto, no todas las llamadas **a ProcessSample** darán como resultado ejemplos de medios de salida.

Si el ejemplo de medios de entrada contiene un fotograma clave indicado por el atributo [**MFSampleExtension \_ CleanPoint,**](mfsampleextension-cleanpoint-attribute.md) el multiplexor copia el atributo en el paquete.

## <a name="getting-asf-data-packets"></a>Obtención de paquetes de datos de ASF

Para recopilar los ejemplos de medios de salida de un paquete de datos completo generado por el multiplexor, llame a [**ALFMultiplexer::GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) en un bucle hasta que no haya más ejemplos de medios de salida para el paquete. A continuación se enumeran los casos de éxito:

-   Si hay un paquete de datos completo disponible, [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) recibe la marca **ASF \_ STATUS \_ FLAGS \_ INCOMPLETE** en el parámetro *pdwStatusFlags;* el parámetro *ppIPacket* recibe un puntero al primer paquete de datos. Debe llamar a este método siempre que reciba esta marca. Con cada iteración, *ppIPacket* apunta al siguiente paquete de la cola.
-   Si solo hay un paquete de datos, *ppIPacket* apunta a él y la marca **ASF \_ STATUS \_ FLAGS \_ INCOMPLETE** no se recibe en *pdwStatusFlags*.
-   [**GetNextPacket puede**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) tener éxito sin producir paquetes de datos si el multiplexor todavía está en proceso de empaquetar paquetes y agregar paquetes de datos. En este caso, *ppIPacket* apunta a **NULL.** Para continuar, debe proporcionar al multiplexor más ejemplos de medios de entrada mediante una llamada [**a ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).

El código de ejemplo siguiente muestra una función que genera paquetes de datos mediante el multiplexor. El contenido del paquete de datos generado se escribirá en el flujo de bytes de datos asignado por el autor de la llamada.


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



La `WriteBufferToByteStream` función se muestra en el tema [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

Para ver una aplicación completa que usa este ejemplo de código, vea Tutorial: Copia de [ASF Secuencias de un archivo a otro.](tutorial--copying-asf-streams-from-one-file-to-another.md)

## <a name="post-packet-generation-calls"></a>Llamadas Packet-Generation posteriores

Para asegurarse de que no hay paquetes de datos completos esperando en el multiplexor, llame a [**MULTICASTASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush). Esto obliga al multiplexor a crear paquetes de todos los ejemplos multimedia que están en curso. La aplicación puede recopilar estos paquetes en forma de ejemplos de medios a través de **GetNextPacket** en un bucle hasta que no haya más paquetes que recuperar.

Una vez generados todos los ejemplos de medios, llame a [**ALFFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) para actualizar el objeto de encabezado asf asociado a estos paquetes de datos. El objeto de encabezado se especifica pasando el objeto ContentInfo que se usó para inicializar el multiplexor. Esta llamada actualiza varios objetos de encabezado para reflejar los cambios realizados por el multiplexor durante la generación de paquetes de datos. Esta información incluye el recuento de paquetes, la duración del envío, la duración de la reproducción y los números de secuencia de todas las secuencias. También se actualiza el tamaño general del encabezado.

Debe asegurarse de que [**se llama**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) a End una vez recuperados todos los paquetes de datos. Si hay paquetes en espera en el multiplexor, **end** producirá un error y devolverá el código de error **MF E FLUSH \_ \_ \_ NEEDED.** En este caso, obtenga el paquete en espera llamando a [**Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) y [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) en un bucle.

> [!Note]  
> Para la codificación de VBR, después de llamar **a End**, debe establecer las estadísticas de codificación en las propiedades de codificación del objeto ContentInfo. Para obtener información sobre este proceso, vea "Configuring the ContentInfo Object with Encoder Configuración" en [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md). En la lista siguiente se muestran las propiedades específicas que se establecerán:
>
> -   [**MFPKEY \_ VBG**](mfpkey-ravgproperty.md) es la velocidad de bits media del contenido de VBR.
> -   [**MFPKEY \_ BAVG es**](mfpkey-bavgproperty.md) la ventana de búfer para la velocidad de bits media.
> -   [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md) es la velocidad de bits máxima del contenido de VBR.
> -   [**MFPKEY \_ BMAX es**](mfpkey-bmaxproperty.md) la ventana de búfer máximo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Multiplexor de ASF](asf-multiplexer.md)
</dt> <dt>

[Tutorial: Copia de asf Secuencias de un archivo a otro](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Tutorial: Escritura de un archivo WMA mediante la codificación CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



