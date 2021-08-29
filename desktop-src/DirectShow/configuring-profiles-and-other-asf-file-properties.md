---
description: Configuración de perfiles y otras propiedades de archivo ASF
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: Configuración de perfiles y otras propiedades de archivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5118c8845506192dac84ca208a7d184023c4a5188d2be372a71be1466d464b6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331005"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a>Configuración de perfiles y otras propiedades de archivo ASF

Los siguientes elementos describen cómo realizar varias tareas relacionadas con la creación de archivos ASF. Algunas de las interfaces mencionadas en este tema se documentan en la documentación Windows SDK de formato multimedia.

Crear un perfil

Los perfiles de ASF se de abordan en detalle en el SDK Windows Media Format; básicamente, describen los atributos de un archivo Windows multimedia, como la velocidad de bits, el número y el tipo de secuencias, y la calidad de compresión. El filtro usa el perfil para determinar qué tipo de archivo de formato multimedia se va Windows escribir, cuántos pines de entrada debe configurar y qué tipos de medios pueden aceptar.

Para crear un perfil personalizado, use el SDK Windows Media Format directamente para crear un objeto de administrador de perfiles mediante la **función WMCreateProfileManager.** A continuación, cree el perfil y pásallo a [WM ASF Writer](wm-asf-writer-filter.md) mediante el [**método IConfigASFWriter::ConfigureFilterUsingProfile.**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) Esta es la única manera de configurar el filtro con un perfil que usa los códecs Windows Media Audio y Video 9 Series. Los perfiles del sistema para versiones anteriores de estos códecs se pueden agregar mediante el método [**IConfigASFWriter::ConfigureFilterUsingProfileGuid.**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid)

Puede restablecer el perfil mientras los pines de entrada del filtro están conectados, siempre y cuando el nuevo perfil no requiera ningún pin de entrada adicional. Por ejemplo, si cambia el perfil de un perfil de solo audio de una entrada a un perfil de audio y vídeo de dos entradas, solo se volverá a conectar la clavija de audio y no se creará ningún nuevo pin para la secuencia de vídeo.

Agregar metadatos

Para agregar metadatos a un archivo, consulte el filtro [WM ASF Writer](wm-asf-writer-filter.md) para la **interfaz IWMHeaderInfo.** Una vez que se ha dado un perfil al filtro, use los métodos de interfaz **IWMHeaderInfo** para escribir los metadatos.

Indexación de un archivo

Wm ASF Writer crea archivos indizados temporalmente de forma predeterminada. Para crear un archivo indexado por fotogramas, use el método [**IConfigAsfWriter::SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) para deshabilitar toda la indexación y, a continuación, cree el archivo. Cuando haya finalizado, use el SDK Windows Media Format directamente para crear un índice basado en fotogramas para el archivo.

Two-Pass codificación

La codificación de dos pases solo se admite Windows códecs multimedia de la versión 8 y posteriores. Coloque WM ASF Writer en modo de preprocesamiento llamando a [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) y especificando AM CONFIGASFWRITER PARAM MULTIPASS en el parámetro dwParam y TRUE en el \_ \_ parámetro \_ *dwParam1.*  

A continuación, ejecute el gráfico de filtro. Cuando se realizan todos los pases de preprocesamiento (normalmente solo se realizará un paso de preprocesamiento), la aplicación recibirá un evento [**\_ EC PREPROCESS \_ COMPLETE**](ec-preprocess-complete.md) del filtro. Cuando se reciba este evento, use [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para restablecer el puntero de secuencia al principio y vuelva a ejecutar el gráfico de filtros. Después del último paso (normalmente el segundo paso), la aplicación recibirá un evento [**EC \_ COMPLETE**](ec-complete.md) para indicar que el proceso de codificación se ha completado. Si se cancela un paso de preprocesamiento antes de recibir el evento **\_ EC PREPROCESS \_ COMPLETE,** llame a [**IConfigAsfWriter2::ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) para restablecer el filtro antes de intentar otra ejecución de preprocesamiento.

Solo es necesario establecer el parámetro MULTIPASS DE AM CONFIGASFWRITER PARAM en FALSE si desea que el filtro salga completamente del modo \_ \_ de \_ preprocesamiento. 

> [!IMPORTANT]
> Es responsabilidad de la aplicación habilitar el modo de preprocesamiento en función del perfil que se usará para la codificación. Algunos perfiles requieren codificación de dos pases; Si intenta codificar un archivo con este tipo de perfil y no establece AM \_ CONFIGASFWRITER PARAM MULTIPASS en TRUE, se producirá un \_ \_ error DE [**\_ USERABORT**](ec-userabort.md) de EC.  Para más información, consulte la documentación del SDK Windows Media Format.

 

Obtención y establecimiento de propiedades de búfer en tiempo de ejecución

En algunos escenarios, por ejemplo, si desea forzar la inserción de fotogramas clave al escribir un archivo, es posible que una aplicación necesite obtener o establecer información sobre un búfer multimedia de Windows en tiempo de ejecución. Los filtros [LECTOR DE ASF](wm-asf-reader-filter.md) de WM y Escritor [ASF](wm-asf-writer-filter.md) de WM admiten un mecanismo de devolución de llamada que permite a una aplicación acceder a la **interfaz INSSBuffer3** en cada búfer multimedia individual durante la lectura de archivos o la escritura de archivos. Las aplicaciones pueden usar esta interfaz para designar ejemplos específicos como fotogramas clave, establecer códigos de tiempo SMPTE, especificar la configuración de interlace o agregar cualquier tipo de datos privados a un flujo.

Use la [**interfaz IAMWMBufferPass para registrarse**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) para las devoluciones de llamada desde el pin que administra la secuencia de vídeo. El pin llamará al [**método IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) para cada búfer.

Píxeles no cuadrados

WM ASF Writer se conecta a un filtro ascendente, como el descodificador DV, que genera información sobre la relación de aspecto de píxeles. WM ASF Writer escribirá esta información como extensiones de unidad de datos para cada ejemplo del archivo.

Cuando el lector DE ASF de WM encuentra información de relación de aspecto de píxel en el encabezado de archivo o en las extensiones de unidad de datos para los ejemplos, ofrecerá un formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) como primera opción en su pin de salida. Los **miembros dwPictAspectRatioX** y **dwPictAspectRatioY** de la estructura, que describen la relación de aspecto del rectángulo de vídeo, se ajustarán correctamente para tener en cuenta la relación de aspecto de píxeles.

Mantener el formato entrelazado

Si captura vídeo entrelazado de una televisión o una cámara DV, es posible que desee conservar el vídeo original como campos independientes si espera que el archivo codificado se re reproduce en un televisor u otro dispositivo de pantalla entrelazado. (Los monitores de equipo son dispositivos de examen progresiva). Si desinterlace un vídeo y, a continuación, lo vuelve a interpretar para su reproducción en una televisión, se incurrirá en una pérdida de datos. En un archivo ASF, la información de entrelazado se almacena como extensiones de unidad de datos que la aplicación aplica a cada ejemplo mediante el método [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) descrito anteriormente. Para codificar un archivo que conserve la configuración de intercalación original, siga estos pasos:

1.  Implemente una clase que **admita IAMWMBufferPassCallback** y escriba una función Notify que establece las marcas de interlace para cada ejemplo. Wm ASF Writer llamará a esta función antes de que procese cada ejemplo.
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

    

3.  Después de configurar el filtro con el perfil, obtenga la interfaz **IWMWriterAdvanced2** desde WM ASF Writer y llame al **método SetInputSettings.**

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

 

 



