---
title: Para crear archivos ASF con códecs de terceros
description: Para crear archivos ASF con códecs de terceros
ms.assetid: 5cd348ca-1f86-429d-92ee-4eab4ced8571
keywords:
- SDK de Windows Media Format, crear archivos ASF
- Windows Media Format SDK, códecs de terceros
- Advanced Systems Format (ASF), crear archivos
- ASF (formato de sistemas avanzados), crear archivos
- Formatos de sistema avanzado (ASF), códecs de terceros
- ASF (formato de sistemas avanzados), códecs de terceros
- códecs de terceros
- códecs, terceros
- códecs, crear archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6c057f1785ed50e328ac6094ff7dbe078e98fc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104358763"
---
# <a name="to-create-asf-files-using-third-party-codecs"></a>Para crear archivos ASF con códecs de terceros

Puede usar el SDK de Windows Media Format para crear archivos ASF que contengan medios digitales codificados con cualquier códec que elija. Al usar un códec distinto de uno incluido en este SDK, debe realizar los pasos siguientes.

1.  Codifique el contenido con el códec deseado.
2.  Busque o cree un valor GUID para identificar el contenido codificado con el códec usado en el paso 1.
3.  Cree un perfil nuevo o modifique uno existente para usarlo con el contenido codificado.
    -   Cree una secuencia para el contenido codificado con el tipo principal adecuado. Para obtener más información acerca de los principales tipos de medios, consulte [tipos de medios](media-types.md). Use el GUID identificado en el paso 2 como el subtipo de medio.
    -   Establezca la velocidad de bits y la ventana de búfer para la secuencia en valores que no producirán un desbordamiento del búfer. Debe poder obtener estos valores del códec en el momento de la codificación. Los componentes en tiempo de ejecución del SDK comprueban los valores de la ventana de velocidad de bits y de búfer y quitan ejemplos si es necesario para que los datos especificados quepan en estos valores. Si establece los valores incorrectamente, el archivo no se transmitirá correctamente, lo que provocará una reproducción deficiente.
    -   En el caso de las secuencias de vídeo, debe establecer el miembro **bicompression** de la estructura **BITMAPINFOHEADER** contenida en la estructura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) en el valor FourCC correspondiente para el contenido. Este valor debe ser igual a los primeros cuatro bytes del GUID del subtipo. Por ejemplo, si la **bicompresión** es MAKEFOURCC (' t ', ' E ', ', ' t ') = 0x54455354, el GUID del subtipo comenzará de la siguiente manera: 54455354-XXXX-XXXX-XXXX-XXXXXXXXXXXX.
4.  Cree un objeto de escritor y cargue el perfil creado en el paso anterior. Para obtener más información acerca de la escritura de archivos, consulte [Writing ASF files](writing-asf-files.md).
5.  Recorra las entradas del archivo y asigne las propiedades de entrada para cada una de ellas como lo haría normalmente. Para obtener más información sobre las entradas, consulte [trabajar con entradas](working-with-inputs.md). En el flujo codificado con un códec de otro fabricante, establezca el puntero de la interfaz [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) en **null** antes de llamar a [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).
6.  Use el nuevo perfil creado en el paso anterior para escribir el archivo. Pase los ejemplos comprimidos mediante [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) en lugar de [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Para vídeo, debe especificar qué ejemplos son fotogramas clave pasando WM \_ SF \_ CLEANPOINT como parámetro *dwFlags* .

Para procesar y descomprimir el flujo codificado con un códec de otro fabricante, debe leer ejemplos de secuencias comprimidas. La aplicación de lectura debe controlar también la descompresión de ejemplo para la secuencia.

## <a name="putting-mpeg-2-streams-into-asf"></a>Colocar secuencias MPEG-2 en ASF

> [!Note]  
> Este tema se aplica a las aplicaciones que usan el SDK de Windows Media Format para colocar MPEG-2 (u otros formatos de compresión que usan fotogramas B) en el contenedor de archivos ASF.

 

El objeto de escritor requiere que todos los ejemplos de entrada tengan marcas de tiempo y se supone que cada ejemplo de entrada tiene un tiempo de presentación posterior al que lo precedía. Aunque prácticamente todo el vídeo sin comprimir e incluso algunos flujos de vídeo comprimidos cumplen estas condiciones, las secuencias MPEG-2 no lo hacen. En MPEG-2, no todos los ejemplos tienen marca de tiempo y, cuando hay fotogramas B, el orden de descodificación de ejemplo no es el mismo que el orden de representación. Cuando el objeto de escritor encuentra ejemplos desordenados, los reorganiza en el orden "correcto". Por lo tanto, para almacenar secuencias MPEG-2 de forma nativa (no descodificada) en un contenedor ASF, debe realizar los siguientes pasos:

Al escribir el archivo:

1.  Agregue una extensión de unidad de datos (debida) de tamaño fijo a cada ejemplo de entrada que contenga una estructura que contenga los valores reales de tiempo de inicio y de finalización de la marca de tiempo MPEG para el ejemplo. Use-1 para estos valores si el ejemplo no tiene ninguna marca de tiempo.
2.  Proporcione a las marcas de tiempo de entrada "ficticios" del objeto de escritor que siempre aumentan para que escriba los ejemplos en el archivo exactamente en el mismo orden en que se reciben. Las marcas de tiempo ficticias deben corresponderse aproximadamente con las horas de presentación reales, como promedio en el tiempo. Las marcas de tiempo ficticias formarán la escala de tiempo de búsqueda, por lo que si difieren en relación con las marcas de tiempo real, las operaciones de búsqueda en el archivo producirán resultados inesperados. Sin embargo, una cantidad limitada de vibración entre las horas de ejemplo no afectará gravemente a las operaciones de búsqueda.

Al leer el archivo:

-   Para cada uno de los ejemplos leídos del archivo, examine el vencimiento. Si contiene una hora de inicio que es mayor o igual que cero, copie el valor en la marca de tiempo para el ejemplo de salida antes de que se entregue al descodificador. Establezca el resto de marcas de tiempo de los ejemplos de salida en **null**. En DirectShow, esto se realiza mediante una llamada a **IMediaSample:: setTime**(**null**,**null**).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Almacenar contenido en búfer**](buffering-content.md)
</dt> <dt>

[**Interfaz IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Interfaz IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Para proporcionar ejemplos comprimidos con el lector asincrónico**](to-deliver-compressed-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Para recuperar ejemplos de secuencias con el lector sincrónico**](to-retrieve-stream-samples-with-the-synchronous-reader.md)
</dt> <dt>

[**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




