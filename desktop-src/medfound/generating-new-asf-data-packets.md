---
description: Generación de nuevos paquetes de datos ASF
ms.assetid: 7afa9694-c965-40e2-8549-e32ff48def2a
title: Generación de nuevos paquetes de datos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f3432ecf34c58247a1533adb202b75f59d770c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496805"
---
# <a name="generating-new-asf-data-packets"></a>Generación de nuevos paquetes de datos ASF

El *multiplexor* ASF es un componente de nivel WMContainer que funciona con el [objeto de datos ASF](asf-file-structure.md) y proporciona a una aplicación la capacidad de generar paquetes de datos ASF para una secuencia que coincida con los requisitos definidos en el objeto ContentInfo.

El multiplexor tiene una entrada y una salida. Recibe un ejemplo de secuencia que contiene datos multimedia digitales y genera uno o más paquetes de datos que se pueden escribir en un contenedor ASF.

En la lista siguiente se resume el proceso de generación de paquetes de datos ASF:

1.  Pase los datos de entrada al multiplexor en [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).
2.  Recopile los paquetes de datos mediante una llamada a [**IMFASFMultiplexer:: GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) en un bucle hasta que se hayan recuperado todos los paquetes completos.
3.  Una vez que los datos de entrada se han convertido en paquetes completos, es posible que haya algunos datos pendientes en el multiplexor, que no se recuperaron mediante [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket). Llame a [**IMFASFMultiplexer:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) para agrupar los ejemplos pendientes y recopilarlos del multiplexor llamando de nuevo a **GetNextPacket** .
4.  Actualice los objetos de encabezado ASF asociados llamando a [**IMFASFMultiplexer:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) para reflejar los cambios realizados por el multiplexor durante la generación de paquetes de datos.

En el diagrama siguiente se ilustra la generación de paquetes de datos para un archivo ASF a través del multiplexor.

![diagrama que muestra la generación de paquetes de datos para un archivo ASF](images/packet.gif)

## <a name="asf-data-packet-creation"></a>Creación de paquetes de datos ASF

Después de crear e inicializar el multiplexor tal y como se describe en [crear el objeto multiplexor](creating-the-multiplexer-object.md), llame a [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) para pasar datos de entrada al multiplexor para su procesamiento en paquetes de datos. La entrada especificada debe estar en un ejemplo multimedia (interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ) que pueda tener uno o más búferes multimedia (interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) ) que contenga los datos de una secuencia. En el caso de la transcodificación ASF a ASF, el ejemplo de medios de entrada se puede generar a partir del divisor que crea ejemplos de secuencias de paquetes. Para obtener más información, consulte separador [ASF](asf-splitter.md).

Antes de llamar a [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), asegúrese de que la marca de tiempo del ejemplo de medios de entrada es un tiempo de presentación válido; de lo contrario, **ProcessSample** produce un error y devuelve el código de marca de tiempo MF \_ e \_ no \_ \_ .

El multiplexor puede aceptar la entrada como muestras de medios comprimidos o sin comprimir a través de [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample). El multiplexor asigna horas de envío a estos ejemplos en función del uso de ancho de banda de la secuencia. Durante este proceso, el multiplexor comprueba los parámetros del depósito de fugas (velocidad de bits y uso de la ventana de búfer) y puede rechazar ejemplos que no se adhieren a esos valores. El ejemplo de medio de entrada puede producir un error en la comprobación de ancho de banda por alguno de los siguientes motivos:

-   Si el ejemplo de medio de entrada llega tarde porque la última hora de envío asignada es mayor que la marca de tiempo de este ejemplo multimedia. [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) produce un error y devuelve el código de error de **\_ ejemplo MF e en \_ tiempo de ejecución \_** .
-   Si la marca de tiempo en el ejemplo de medio de entrada es anterior a la hora de envío asignada (esto indica el desbordamiento del búfer). El multiplexor puede omitir esta situación si está configurada para ajustar la velocidad de bits mediante el establecimiento de la marca de velocidad de bits **\_ \_ autoajuste \_ del multiplexor de MFASF** durante la inicialización del multiplexor. Para obtener más información, vea "configuración de la inicialización del multiplexor y del depósito de fugas" en [crear el objeto multiplexor](creating-the-multiplexer-object.md). Si no se establece esta marca y el multiplexor detecta la saturación del ancho de banda, [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) produce un error y devuelve el código de error de saturación de **ancho de banda de MF \_ E \_ \_** .

Una vez que el multiplexor asigna la hora de envío, el ejemplo de medio de entrada se agrega a la *ventana de envío*: una lista de ejemplos de medios de entrada ordenados por horas de envío y listas para su procesamiento en paquetes de datos. Durante la construcción de paquetes de datos, se analiza el ejemplo de medios de entrada y los datos relevantes se escriben en un paquete de datos como carga. Un paquete de datos completo puede contener datos de uno o más ejemplos de medios de entrada.

Cuando llegan los nuevos ejemplos de medios de entrada en la ventana de envío, se agregan a una cola hasta que hay suficientes ejemplos de medios para formar un paquete completo. Los datos de los búferes multimedia contenidos en el ejemplo de medios de entrada no se copian en el paquete de datos generado. El paquete de datos mantiene referencias a los búferes de los medios de entrada hasta que el ejemplo de medios de entrada se ha descargado por completo y se ha recopilado el paquete completo del multiplexor.

Cuando hay un paquete de datos completo disponible, se puede recuperar llamando a [**IMFASFMultiplexer:: GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket). Si llama a [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) mientras hay paquetes completos listos para su recuperación, se produce un error y se devuelve el código de error **MF \_ e \_ NOTACCEPTING** . Esto indica que el multiplexor no puede aceptar más entradas y debe llamar a **GetNextPacket** para recuperar los paquetes en espera. Idealmente, todas las llamadas a **ProcessSample** deben ir seguidas de una o varias llamadas de **GetNextPacket** para obtener los paquetes de datos completos. Puede tomar más de un ejemplo de medios de entrada para crear un paquete de datos completo. Por el contrario, los datos de un ejemplo de medios de entrada pueden abarcar varios paquetes. Por lo tanto, no todas las llamadas a **ProcessSample** producirán ejemplos de medios de salida.

Si el ejemplo de medio de entrada contiene un fotograma clave indicado por el atributo [**\_ CleanPoint de MFSampleExtension**](mfsampleextension-cleanpoint-attribute.md) , el multiplexor copia el atributo en el paquete.

## <a name="getting-asf-data-packets"></a>Obtener paquetes de datos ASF

Para recopilar los ejemplos de medios de salida de un paquete de datos completo generado por el multiplexor, llame a [**IMFASFMultiplexer:: GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) en un bucle hasta que no queden más muestras de medios de salida para el paquete. A continuación se enumeran los casos de éxito:

-   Si hay un paquete de datos completo disponible, [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) recibe la marca **ASF \_ status \_ Flags \_ incompleta** en el parámetro *pdwStatusFlags* ; el parámetro *ppIPacket* recibe un puntero al primer paquete de datos. Debe llamar a este método siempre que reciba esta marca. Con cada iteración, *ppIPacket* apunta al siguiente paquete de la cola.
-   Si solo hay un paquete de datos, *ppIPacket* apunta a él y no se recibe la marca de **marcas de estado de ASF \_ \_ \_ incompletas** en *pdwStatusFlags*.
-   [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) puede realizarse sin producir paquetes de datos si el multiplexor todavía está en proceso de paquetes y agregando paquetes de datos. En este caso, *ppIPacket* apunta a **null**. Para continuar, debe proporcionar al multiplexor más ejemplos de medios de entrada mediante una llamada a [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).

En el ejemplo de código siguiente se muestra una función que genera paquetes de datos mediante el multiplexor. El contenido del paquete de datos generado se escribirá en la secuencia de bytes de datos asignada por el llamador.


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



La `WriteBufferToByteStream` función se muestra en el tema [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

Para ver una aplicación completa que utiliza este ejemplo de código, vea [Tutorial: copiar secuencias ASF de un archivo a otro](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="post-packet-generation-calls"></a>Llamadas Packet-Generation posteriores

Para asegurarse de que no haya paquetes de datos completos en espera en el multiplexor, llame a [**IMFASFMultiplexer:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush). Esto obliga al multiplexor a paquetes a todos los ejemplos de medios que están en curso. La aplicación puede recopilar estos paquetes en forma de muestras de medios a través de **GetNextPacket** en un bucle hasta que no quedan más paquetes para recuperar.

Una vez generados todos los ejemplos de medios, llame a [**IMFASFMultiplexer:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) para actualizar el objeto de encabezado ASF que está asociado a estos paquetes de datos. El objeto de encabezado se especifica pasando el objeto ContentInfo que se usó para inicializar el multiplexor. Esta llamada actualiza varios objetos de encabezado para reflejar los cambios realizados por el multiplexor durante la generación de paquetes de datos. Esta información incluye el número de paquetes, la duración del envío, la duración de la reproducción y los números de secuencia de todos los flujos. También se actualiza el tamaño total del encabezado.

Debe asegurarse de que se llama a [**End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) una vez recuperados todos los paquetes de datos. Si hay paquetes en espera en el multiplexor, **End** producirá un error y devolverá el código de error de **\_ vaciado de MF E \_ \_ necesario** . En este caso, obtenga el paquete en espera llamando a [**Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) y [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) en un bucle.

> [!Note]  
> En el caso de la codificación VBR, después de llamar a **End**, debe establecer las estadísticas de codificación en las propiedades de codificación del objeto ContentInfo. Para obtener información sobre este proceso, vea "configurar el objeto ContentInfo con la configuración del codificador" en [establecer propiedades en el objeto ContentInfo](setting-properties-in-the-contentinfo-object.md). En la lista siguiente se muestran las propiedades específicas que se deben establecer:
>
> -   [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md) es la velocidad de bits promedio del contenido de VBR.
> -   [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md) es la ventana de búfer para la velocidad de bits media.
> -   [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md) es la velocidad de bits máxima del contenido de VBR.
> -   [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) es la ventana de búfer máximo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Multiplexor ASF](asf-multiplexer.md)
</dt> <dt>

[Tutorial: copiar secuencias ASF de un archivo a otro](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Tutorial: escribir un archivo WMA con codificación CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



