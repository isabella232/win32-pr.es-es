---
title: Para crear archivos ASF mediante códecs de terceros
description: Para crear archivos ASF mediante códecs de terceros
ms.assetid: 5cd348ca-1f86-429d-92ee-4eab4ced8571
keywords:
- Windows SDK de formato multimedia, creación de archivos ASF
- Windows SDK de formato multimedia, códecs de terceros
- Formato de sistemas avanzados (ASF), crear archivos
- ASF (formato de sistemas avanzados), crear archivos
- Formato de sistemas avanzados (ASF), códecs de terceros
- ASF (formato de sistemas avanzados), códecs de terceros
- códecs de terceros
- códecs, de terceros
- códecs, creación de archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1eeeb891037581a550d8c15c2f2b4cefa14f81f20d0d55623d382d0e933e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197085"
---
# <a name="to-create-asf-files-using-third-party-codecs"></a>Para crear archivos ASF mediante códecs de terceros

Puede usar el SDK Windows Media Format para crear archivos ASF que contengan medios digitales codificados con cualquier códec que elija. Al usar un códec distinto de uno incluido con este SDK, debe realizar los pasos siguientes.

1.  Codifica el contenido con el códec deseado.
2.  Busque o cree un valor GUID para identificar el contenido codificado con el códec usado en el paso 1.
3.  Cree un perfil o modifique uno existente para usarlo con el contenido codificado.
    -   Cree una secuencia para el contenido codificado con el tipo principal adecuado. Para obtener más información sobre los tipos de medios principales, vea [Tipos de medios](media-types.md). Use el GUID identificado en el paso 2 como subtipo de medio.
    -   Establezca la velocidad de bits y la ventana de búfer de la secuencia en valores que no darán lugar a desbordamiento del búfer. Debería poder obtener estos valores del códec en el momento de la codificación. Los componentes en tiempo de ejecución del SDK comprueban los valores de la ventana de búfer/velocidad de bits y quitar ejemplos si es necesario para que los datos determinados se ajusten a estos valores. Si establece los valores incorrectamente, el archivo no se transmitirá correctamente, lo que provocará una reproducción deficiente.
    -   Para las secuencias de vídeo, debe establecer el miembro **biCompression** de la estructura **BITMAPINFOHEADER** contenida en la estructura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) en el valor FOURCC adecuado para el contenido. Este valor debe ser igual a los cuatro primeros bytes del GUID del subtipo. Por ejemplo, si **biCompression** es MAKEFOURCC('T','E','S','T')=0x54455354, el GUID del subtipo comenzará de la siguiente forma: 54455354-XXXX-XXXX-XXXX-XXXXXXXXXXXX.
4.  Cree un objeto de escritor y cargue el perfil creado en el paso anterior. Para obtener más información sobre cómo escribir archivos, vea [Escribir archivos ASF](writing-asf-files.md).
5.  Recorrer en bucle las entradas del archivo y asignar propiedades de entrada para cada una de ellas como lo haría normalmente. Para obtener más información sobre las entradas, vea [Trabajar con entradas](working-with-inputs.md). Para la secuencia codificada con un códec de terceros, establezca el puntero de interfaz [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) en **NULL** antes de llamar a [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).
6.  Use el nuevo perfil creado en el paso anterior para escribir el archivo. Pase los ejemplos comprimidos mediante [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) en lugar de [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Para el vídeo, debe especificar qué ejemplos son fotogramas clave pasando WM \_ SF \_ CLEANPOINT como parámetro *dwFlags.*

Para procesar y descomprimir la secuencia codificada con un códec de terceros, debe leer ejemplos de secuencias comprimidas. La aplicación de lectura también debe controlar la descompresión de ejemplo para la secuencia.

## <a name="putting-mpeg-2-streams-into-asf"></a>Colocación de secuencias MPEG-2 en ASF

> [!Note]  
> Este tema se aplica a las aplicaciones que usan el SDK de formato multimedia de Windows para colocar MPEG-2 (u otros formatos de compresión que usan fotogramas B) en el contenedor de archivos ASF.

 

El objeto de escritor requiere que todas las muestras de entrada tengan marcas de tiempo y supone que cada muestra de entrada tiene un tiempo de presentación posterior al anterior. Aunque prácticamente todos los vídeos sin comprimir e incluso algunas secuencias de vídeo comprimidas cumplen estas condiciones, las secuencias MPEG-2 no lo hacen. En MPEG-2, no todas las muestras tienen marca de tiempo y, cuando hay fotogramas B presentes, el orden de la codificación de ejemplo no es el mismo que el orden de representación. Cuando el objeto de escritor encuentra ejemplos desordenados, los reorganiza en el orden "correcto". Por lo tanto, para almacenar secuencias MPEG-2 de forma nativa (no descodificadas) en un contenedor de ASF, debe realizar los pasos siguientes:

Al escribir el archivo:

1.  Agregue una extensión de unidad de datos de tamaño fijo (DUE) a cada muestra de entrada que contendrá una estructura que contiene los valores reales de hora de inicio y de detenerse de marca de tiempo MPEG para el ejemplo. Use -1 para estos valores si el ejemplo no tiene marca de tiempo.
2.  Dé al objeto de escritor marcas de tiempo de entrada "ficticias" que siempre aumentan para que escriba los ejemplos en el archivo exactamente en el mismo orden en que se reciben. Las marcas de tiempo ficticias deben corresponder aproximadamente a los tiempos de presentación reales, como se promedia con el tiempo. Las marcas de tiempo ficticias formarán la escala de tiempo de búsqueda, por lo que si divergen en relación con las marcas de tiempo real, las operaciones de búsqueda en el archivo producirán resultados inesperados. Sin embargo, una cantidad limitada de vibración entre los tiempos de muestra no afectará gravemente a las operaciones de búsqueda.

Al leer el archivo:

-   Para cada ejemplo leído del archivo, examine due. Si contiene una hora de inicio mayor o igual que cero, copie ese valor en la marca de tiempo del ejemplo de salida antes de entregarlo al descodificador. Establezca el resto de marcas de tiempo de los ejemplos de salida en **NULL.** En DirectShow, esto se realiza mediante una llamada a **IMediaSample::SetTime**(**NULL**,**NULL**).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Almacenamiento en búfer de contenido**](buffering-content.md)
</dt> <dt>

[**IWMWriter (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**IWMWriterAdvanced (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Para entregar ejemplos comprimidos con el lector asincrónico**](to-deliver-compressed-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Para recuperar ejemplos de secuencia con el lector sincrónico**](to-retrieve-stream-samples-with-the-synchronous-reader.md)
</dt> <dt>

[**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




