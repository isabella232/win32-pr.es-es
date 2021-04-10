---
description: Generar ejemplos de secuencia a partir de un objeto de datos ASF existente
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Generar ejemplos de secuencia a partir de un objeto de datos ASF existente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee612c9352e3295d6b4957922e385de40a9a1fa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153629"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a>Generar ejemplos de secuencia a partir de un objeto de datos ASF existente

El objeto de *separador* ASF es un componente de nivel WMContainer que analiza el objeto de datos ASF de un archivo de formato de sistema avanzado (ASF).

Antes de pasar paquetes de datos al divisor, la aplicación debe inicializar, configurar y seleccionar secuencias en el divisor para prepararlo para el proceso de análisis. Para obtener más información, vea [crear el objeto divisor de ASF](creating-the-asf-splitter-object.md) y [configurar el objeto divisor de ASF](configuring-the-asf-splitter-object.md).

Los métodos necesarios para analizar el objeto de datos ASF son:

-   [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) que inicia el proceso de análisis insertando el búfer que contiene los paquetes de datos en el divisor.
-   [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) que recopila ejemplos de secuencias generados a partir del búfer pasado al divisor.

## <a name="finding-the-data-offset"></a>Buscar el desplazamiento de datos

Antes de iniciar el proceso de análisis, la aplicación debe buscar el objeto de datos en el archivo ASF. Hay dos maneras de obtener el desplazamiento del objeto de datos desde el principio del archivo:

-   Antes de inicializar el objeto ContentInfo, puede llamar al método [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) . Este método requiere un búfer que contenga los primeros 30 bytes del encabezado ASF. Devuelve el tamaño del encabezado completo que indica el desplazamiento al primer paquete de datos. Este valor también incluye el tamaño del encabezado del objeto de datos de 50 bytes.
-   Después de inicializar el objeto ContentInfo, puede obtener el descriptor de presentación llamando a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)y, a continuación, consultando el descriptor de presentación para el atributo de [**desplazamiento de \_ \_ \_ \_ Inicio \_ de datos ASF de MF PD**](mf-pd-asf-data-start-offset-attribute.md) . El valor de este atributo es el tamaño del encabezado.
    > [!Note]  
    > El atributo de [**\_ \_ \_ \_ longitud de datos ASF de MF**](mf-pd-asf-data-length-attribute.md) en el descriptor de presentación especifica la longitud del objeto de datos ASF.

     

En ambos casos, el valor devuelto es el tamaño del objeto de encabezado más el tamaño de la sección de encabezado del objeto de datos. Por lo tanto, el valor resultante es el desplazamiento al inicio de los paquetes de datos en el objeto de datos ASF. Cuando empiece a enviar datos al divisor, los datos deben comenzar en este desplazamiento desde el principio del archivo ASF.

El valor de desplazamiento se pasa como un parámetro a **ParseData** que inicia el proceso de análisis.

El objeto de datos se divide en paquetes de datos. Cada paquete de datos contiene un encabezado de paquete de datos que proporciona información de análisis de paquetes y los datos de carga, los datos de medios digitales reales. En un escenario de búsqueda, la aplicación podría querer que el divisor iniciara el análisis en un paquete de datos determinado. Para ello, puede usar el indizador ASF para recuperar el desplazamiento. El indexador devuelve un valor de desplazamiento que comienza en el límite del paquete. Si no usa el indexador, asegúrese de que el desplazamiento comienza al principio del encabezado del paquete de datos. Si se pasa un desplazamiento no válido al divisor, como el valor no apunta al límite del paquete, las llamadas a **ParseHeader** y **GetNextSample** se realizan correctamente pero **GetNextSample** no recupera ningún ejemplo y se recibe **null** en el parámetro *pSample* .

Si el divisor está configurado para analizar en dirección inversa, el divisor siempre comienza el análisis al final del búfer de medios que se pasa a **ParseData**. Por lo tanto, para el análisis inverso en la llamada a **ParseData**, pase el desplazamiento en el parámetro *cbLength* , que especifica la longitud de los datos y establece *cbBufferOffset* en cero.

## <a name="generating-samples-for-asf-data-packets"></a>Generar ejemplos para paquetes de datos ASF

Una aplicación inicia el proceso de análisis pasando los paquetes de datos al divisor. La entrada del divisor es una serie de búferes multimedia que contienen los fragmentos completos del objeto de datos. La salida del divisor es una serie de ejemplos de medios que contienen los datos del paquete.

Para pasar datos de entrada al divisor, cree un búfer de medios y rellénelo con los datos de la sección del objeto de datos del archivo ASF. (Para obtener más información sobre los búferes multimedia, consulte [búferes multimedia](media-buffers.md)). A continuación, pase el búfer multimedia al método [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) . También puede especificar:

-   Desplazamiento en el búfer donde el divisor debe empezar a analizar. Si el desplazamiento es cero, el análisis comienza en el inicio del búfer. Para obtener información acerca de cómo establecer el desplazamiento de datos, vea la sección "buscar el desplazamiento de datos" de este tema.
-   La cantidad de datos que se van a analizar. Si este valor es cero, el divisor se analiza hasta que alcanza el final del búfer, tal y como se especifica en el método [**IMFMediaBuffer:: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) .

El divisor genera ejemplos de medios haciendo referencia a los datos de los búferes multimedia. El cliente puede recuperar los ejemplos de salida llamando a [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) en un bucle hasta que no haya más datos para analizar. Si **GetNextSample** devuelve la \_ \_ marca de ASF STATUSFLAGS incompleta en el parámetro *pdwStatusFlags* , significa que hay más ejemplos para recuperar y la aplicación puede volver a llamar a **GetNextSample** . De lo contrario, llame a **ParseData** para pasar más datos al divisor. En el caso de los ejemplos generados, el divisor establece la información siguiente:

-   El divisor establece una marca de tiempo en todos los ejemplos que genera. La hora de muestra representa el tiempo de presentación y no incluye el tiempo de preestación. La aplicación puede llamar a [**IMFSample:: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) para obtener el tiempo de presentación, en unidades de 100-nanosegundos.
-   Si se produce una interrupción durante la generación del ejemplo, el divisor establece el atributo [**\_ discontinuidad MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) en el primer ejemplo después de la discontinuidad. Las discontinuidades suelen deberse a la pérdida de paquetes en una conexión de red, a datos de archivos dañados o a la conmutación de divisores de un flujo de origen a otro.
-   En el caso de vídeo, el divisor comprueba si el ejemplo contiene un fotograma clave. Si lo hace, el divisor establece el atributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) en el ejemplo.

Si el divisor analiza los paquetes de datos que se reciben de un servidor multimedia, es posible que la longitud del paquete sea variable. En este caso, el cliente debe llamar a **ParseData** para cada paquete y establecer el atributo de [**\_ \_ límite de paquetes MFASFSPLITTER**](mfasfsplitter-packet-boundary-attribute.md) en cada búfer que se envía al divisor. Este atributo indica al divisor si el búfer multimedia contiene el inicio de un paquete ASF. Establezca el atributo en **true** si el búfer contiene el inicio de un nuevo paquete. Si el búfer contiene una continuación del paquete anterior, establezca el atributo en **false**. Los búferes no pueden abarcar varios paquetes.

Antes de pasar nuevos búferes multimedia al divisor, la aplicación debe llamar a [**IMFASFSplitter:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush). Este método restablece el divisor y borra cualquier fotograma parcial que esté a la espera de que se complete. Esto resulta útil en un escenario de búsqueda en el que el desplazamiento está en una ubicación diferente.

### <a name="example"></a>Ejemplo

En el ejemplo de código siguiente se muestra cómo analizar paquetes de datos. En este ejemplo se analiza desde el principio del objeto de datos hasta el final de la secuencia y se muestra información acerca de los ejemplos que contienen fotogramas clave. Para obtener un ejemplo completo que usa este código, vea [Tutorial: leer un archivo ASF](tutorial--reading-an-asf-file.md).


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Divisor ASF](asf-splitter.md)
</dt> </dl>

 

 



