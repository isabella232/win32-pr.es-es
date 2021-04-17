---
description: Escribir un proyecto en un archivo
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Escribir un proyecto en un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f63ddbc6a021362134d420220f7e25c662553f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687719"
---
# <a name="writing-a-project-to-a-file"></a>Escribir un proyecto en un archivo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En este artículo se describe cómo escribir un proyecto de [servicios de edición de DirectShow](directshow-editing-services.md) en un archivo. En primer lugar, se describe cómo escribir un archivo con el motor de representación básico. A continuación, se describe la recompresión inteligente con el motor de representación inteligente.

Para obtener información general sobre cómo los servicios de edición de DirectShow representan proyectos, consulte [acerca de los motores de representación](about-the-render-engines.md).

**Usar el motor de representación básico**

Empiece por crear el front-end del gráfico, como se indica a continuación:

1.  Cree el motor de representación.
2.  Especifique la escala de tiempo.
3.  Establezca el intervalo de representación. (Opcional)
4.  Cree el front-end del gráfico.

En el ejemplo de código siguiente se muestran estos pasos.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



A continuación, agregue filtros multiplexores y de escritura de archivos al gráfico de filtros. La forma más fácil de hacerlo es con el [generador de gráficos de captura](capture-graph-builder.md), un componente de DirectShow para crear gráficos de captura. El generador de gráficos de captura expone la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . Lleve a cabo los siguiente pasos:

1.  Cree una instancia del generador de gráficos de captura.
2.  Obtenga un puntero al gráfico y páselo al generador de gráficos.
3.  Especifique el nombre y el tipo de medio del archivo de salida. Este paso también obtiene un puntero al filtro MUX, que es necesario más adelante.

En el ejemplo de código siguiente se muestran estos pasos.


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



Por último, conecte los terminales de salida en el front-end al filtro Mux.

1.  Recupere el número de grupos.
2.  Para cada pin, obtenga un puntero al pin.
3.  Opcionalmente, cree una instancia de un filtro de compresión para comprimir la secuencia. El tipo de compresor dependerá del tipo de medio del grupo. Puede usar el [enumerador de dispositivos del sistema](system-device-enumerator.md) para enumerar los filtros de compresión disponibles. Para obtener más información, vea [enumerar dispositivos y filtros](enumerating-devices-and-filters.md).
4.  Opcionalmente, establezca parámetros de compresión como la velocidad de fotogramas clave. Este paso se describe en detalle más adelante en el artículo.
5.  Llame a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream). Este método toma punteros al pin, el filtro de compresión (si existe) y el multiplexor.

En el ejemplo de código siguiente se muestra cómo conectar los pin de salida.


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



Para establecer los parámetros de compresión (el paso 4, anteriormente), use la interfaz [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) . Esta interfaz se expone en las clavijas de salida de los filtros de compresión. Enumere los PIN del filtro de compresión y consulte cada pin de salida para **IAMVideoCompression**. (Para obtener información sobre la enumeración de los pin, consulte [enumeración de PIN](enumerating-pins.md)). Asegúrese de liberar todos los punteros de interfaz obtenidos durante este paso.

Después de compilar el gráfico de filtros, llame al método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) en el administrador de gráficos de filtro. A medida que se ejecuta el gráfico de filtros, escribe los datos en un archivo. Use la notificación de eventos para esperar a que se complete la reproducción. (Consulte [responder a eventos](responding-to-events.md)). Cuando finalice la reproducción, debe llamar explícitamente a [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) para detener el gráfico de filtro. De lo contrario, el archivo no se escribe correctamente.

**Usar el motor de representación inteligente**

Para obtener las ventajas de la recompresión inteligente, utilice el motor de representación inteligente en lugar del motor de representación básico. Los pasos para generar el gráfico son prácticamente los mismos. La principal diferencia es que la compresión se controla en el front-end del gráfico, no en la sección de escritura de archivos.

> [!IMPORTANT]
> No utilice el motor de representación inteligente para leer o escribir archivos de Windows Media.

 

Cada grupo de vídeos tiene una propiedad que especifica el formato de compresión para ese grupo. El formato de compresión debe coincidir exactamente con el formato sin comprimir del grupo en el alto, el ancho, la profundidad de bits y la velocidad de fotogramas. El motor de representación inteligente usa el formato de compresión al construir el gráfico. Antes de establecer el formato de compresión, asegúrese de establecer el formato sin comprimir para ese grupo mediante una llamada a [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md).

Para establecer el formato de compresión de un grupo, llame al método [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) . Este método toma un puntero a una estructura [**SCompFmt0**](scompfmt0.md) . La estructura **SCompFmt0** tiene dos miembros: **nFormatId**, que debe ser cero y **mediatype**, que es una estructura [**de \_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Inicialice la estructura de **\_ \_ tipo de medio am** con la información de formato.

> [!Note]  
> Si desea que el proyecto final tenga el mismo formato que uno de los archivos de origen, puede obtener la \_ \_ estructura de tipo de medio am directamente desde el archivo de origen, mediante el detector de medios. Vea [**IMediaDet:: get \_ StreamMediaType**](imediadet-get-streammediatype.md).

 

Convierta la variable [**SCompFmt0**](scompfmt0.md) en un puntero de tipo **Long**, tal como se muestra en el ejemplo siguiente.


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



El motor de representación inteligente busca automáticamente un filtro de compresión compatible. También puede especificar un filtro de compresión para un grupo mediante una llamada a [**ISmartRenderEngine:: SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).

Para compilar el gráfico, siga los mismos pasos descritos para el motor de representación básico en la sección anterior. Las únicas diferencias son las siguientes:

-   Use el motor de representación inteligente, no el motor de representación básico. El identificador de clase es CLSID \_ SmartRenderEngine.
-   Establezca los parámetros de compresión después de compilar el front-end, pero antes de representar los pines de salida. Llame al método [**ISmartRenderEngine:: GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) para obtener un puntero al filtro de compresión de un grupo. A continuación, consulte la interfaz [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , tal y como se describió anteriormente.
-   Al representar los pines de salida, no es necesario insertar un filtro de compresión. La secuencia ya está comprimida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar un proyecto](rendering-a-project.md)
</dt> </dl>

 

 



