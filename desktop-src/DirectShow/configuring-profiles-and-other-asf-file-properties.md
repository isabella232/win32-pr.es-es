---
description: Configuración de perfiles y otras propiedades de archivo ASF
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: Configuración de perfiles y otras propiedades de archivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422996"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a>Configuración de perfiles y otras propiedades de archivo ASF

En los elementos siguientes se describe cómo realizar varias tareas relacionadas con la creación de archivos ASF. Algunas de las interfaces mencionadas en este tema se documentan en la documentación del SDK de Windows Media Format.

Creación de un perfil

Los perfiles ASF se describen en detalle en el SDK de Windows Media Format; en esencia, describen los atributos de un archivo de formato de Windows Media, como la velocidad de bits, el número y el tipo de secuencias, y la calidad de la compresión. El filtro usa el perfil para determinar el tipo de archivo de formato de Windows Media que se va a escribir, el número de clavijas de entrada que debe configurar y los tipos de medios que pueden aceptar.

Para crear un perfil personalizado, use el SDK de Windows Media Format directamente para crear un objeto de administrador de perfiles mediante la función **WMCreateProfileManager** . A continuación, cree el perfil y páselo al escritor de [ASF de WM](wm-asf-writer-filter.md) mediante el método [**IConfigASFWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) . Esta es la única manera de configurar el filtro con un perfil que use los códecs de la serie Windows Media Audio y vídeo 9. Los perfiles de sistema para versiones anteriores de estos códecs se pueden agregar mediante el método [**IConfigASFWriter:: ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) .

Puede restablecer el perfil mientras los pines de entrada del filtro están conectados, siempre que el nuevo perfil no requiera ninguna clavija de entrada adicional. Por ejemplo, si cambia el perfil de un perfil de sólo audio de una entrada a un perfil de audio y vídeo de dos entradas, solo se volverá a conectar el PIN de audio y no se creará ningún PIN nuevo para la secuencia de vídeo.

Agregar metadatos

Para agregar metadatos a un archivo, consulte el filtro de [escritor ASF de WM](wm-asf-writer-filter.md) para la interfaz **IWMHeaderInfo** . Una vez que se ha dado un perfil al filtro, use los métodos de la interfaz **IWMHeaderInfo** para escribir los metadatos.

Indexación de un archivo

De manera predeterminada, el escritor ASF de WM crea archivos indizados de forma temporal. Para crear un archivo indexado mediante Marcos, use el método [**IConfigAsfWriter:: SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) para deshabilitar toda la indexación y, a continuación, cree el archivo. Cuando haya finalizado, use el SDK de Windows Media Format directamente para crear un índice basado en marco para el archivo.

Codificación de Two-Pass

La codificación de dos pasos solo se admite en códecs de Windows Media de la versión 8 y posteriores. Coloque el escritor ASF de WM en modo de preprocesamiento llamando a [**IConfigAsfWriter2:: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) y especificando AM \_ CONFIGASFWRITER \_ param \_ Multipass en el parámetro *DwParam* y **true** en el parámetro *dwParam1* .

A continuación, ejecute el gráfico de filtro. Cuando se realizan todos los pasos de preprocesamiento (normalmente solo se realizará un paso de preprocesamiento), la aplicación recibirá un evento de [**\_ \_ finalización de preprocesamiento de EC**](ec-preprocess-complete.md) del filtro. Cuando se reciba este evento, use [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para restablecer el puntero de secuencia de nuevo al principio y vuelva a ejecutar el gráfico de filtro. Después del último paso (normalmente el segundo paso), la aplicación recibirá un evento de [**\_ finalización de EC**](ec-complete.md) para indicar que se ha completado el proceso de codificación. Si se cancela un paso de preprocesamiento antes de que se reciba el evento de **\_ \_ finalización** previa al preprocesamiento, llame a [**IConfigAsfWriter2:: ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) para restablecer el filtro antes de intentar otra ejecución de preprocesamiento.

Solo es necesario establecer el \_ parámetro AM CONFIGASFWRITER \_ param \_ Multipass en **false** si desea dejar por completo el filtro del modo de preprocesamiento.

> [!IMPORTANT]
> Es responsabilidad de la aplicación habilitar el modo de preprocesamiento basado en el perfil que se utilizará para la codificación. Algunos perfiles requieren codificación de dos pasos; Si intenta codificar un archivo con este tipo de perfil y no establece AM \_ CONFIGASFWRITER \_ param \_ Multipass en **true**, se producirá un error de [**\_ USERABORT de EC**](ec-userabort.md) . Para obtener más información, consulte la documentación del SDK de Windows Media Format.

 

Obtener y establecer propiedades de búfer en tiempo de ejecución

En algunos escenarios, por ejemplo, si desea forzar la inserción de fotogramas clave al escribir un archivo, es posible que una aplicación necesite obtener o establecer información sobre un búfer de Windows Media en tiempo de ejecución. Los filtros del [lector ASF de WM](wm-asf-reader-filter.md) y del [escritor ASF de WM](wm-asf-writer-filter.md) admiten un mecanismo de devolución de llamada que permite a una aplicación tener acceso a la interfaz **INSSBuffer3** en cada búfer multimedia individual durante la lectura o escritura de archivos. Las aplicaciones pueden usar esta interfaz para designar ejemplos específicos como fotogramas clave, establecer códigos de tiempo SMPTE, especificar la configuración de entrelazado o agregar cualquier tipo de datos privados a un flujo.

Use la interfaz [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) para registrar las devoluciones de llamada del PIN que está controlando la secuencia de vídeo. El PIN llamará al método [**IAMWMBufferPassCallback:: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) para cada búfer.

Píxeles no cuadrados

El escritor ASF de WM se conecta a un filtro de nivel superior, como el descodificador DV, que genera información de relación de aspecto de píxeles. El escritor ASF de WM escribirá esta información como extensiones de unidad de datos para cada muestra del archivo.

Cuando el lector ASF de WM encuentra información de relación de aspecto de píxeles en el encabezado de archivo o en las extensiones de unidad de datos para los ejemplos, ofrecerá un formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) como primera opción en el PIN de salida. Los miembros **dwPictAspectRatioX** y **dwPictAspectRatioY** de la estructura, que describen la relación de aspecto del rectángulo de vídeo, se ajustarán correctamente para tener en cuenta la relación de aspecto de píxeles.

Mantener el formato entrelazado

Si captura vídeo entrelazado de una cámara de televisión o DV, es posible que desee conservar el vídeo original como campos independientes si espera que el archivo codificado se reproduzca en un televisor u otro dispositivo de pantalla entrelazada. (Los monitores de equipos son dispositivos de digitalización progresiva). Si desentrelaza un vídeo y, a continuación, lo reentrelaza para su reproducción en un televisor, se producirá una pérdida de datos. En un archivo ASF, la información de entrelazado se almacena como extensiones de unidad de datos que la aplicación aplica a cada ejemplo mediante el método [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) descrito anteriormente. Para codificar un archivo que conserva la configuración de entrelazado original, siga estos pasos:

1.  Implemente una clase que admita **IAMWMBufferPassCallback** y escriba una función Notify que establezca las marcas de entrelazado para cada ejemplo. El escritor ASF de WM llamará a esta función antes de procesar cada ejemplo.
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  Establezca las extensiones de unidad de datos en el perfil antes de pasar el perfil al filtro.
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  Después de configurar el filtro con el perfil, obtenga la interfaz **IWMWriterAdvanced2** del escritor ASF de WM y llame al método **SetInputSettings** .

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
    CComPtr<IServiceProvider> pProvider;
    CComPtr<IWMWriterAdvanced2> pWMWA2;

    hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                             (void**)&pProvider);
    if (SUCCEEDED(hr))
    {
        hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
            IID_IWMWriterAdvanced2,
            (void**)&pWMWA2);
    }

    BOOL pValue = TRUE;

    // Set the first parameter to your actual input number.
    hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
        WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
                
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



