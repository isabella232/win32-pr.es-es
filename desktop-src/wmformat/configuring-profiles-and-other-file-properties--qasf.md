---
title: Configuración de perfiles y otras propiedades de archivo (QASF)
description: Configuración de perfiles y otras propiedades de archivo (QASF)
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- Windows SDK de formato multimedia, configuración de perfiles (QASF)
- Windows SDK de formato multimedia, configuración de propiedades de archivo (QASF)
- Windows SDK de formato multimedia, metadatos (QASF)
- Formato de sistemas avanzados (ASF), configuración de perfiles (QASF)
- ASF (formato de sistemas avanzados), configuración de perfiles (QASF)
- Formato de sistemas avanzados (ASF), configurar propiedades de archivo (QASF)
- ASF (formato de sistemas avanzados), configurar propiedades de archivo (QASF)
- Formato de sistemas avanzados (ASF),metadatos (QASF)
- ASF (formato de sistemas avanzados), metadatos (QASF)
- Windows SDK de formato multimedia, QASF
- Formato de sistemas avanzados (ASF),QASF
- ASF (formato de sistemas avanzados),QASF
- metadata,QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251552"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a>Configuración de perfiles y otras propiedades de archivo (QASF)

Los siguientes elementos describen cómo realizar varias tareas relacionadas con la creación de archivos ASF.

## <a name="creating-a-profile-qasf"></a>Crear un perfil (QASF)

Para crear un perfil personalizado, use Windows SDK de formato multimedia directamente para crear un objeto de administrador de perfiles mediante la [**función WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) A continuación, cree el perfil y pásallo a [WM ASF Writer](wm-asf-writer-filter.md) mediante el [**método IConfigASFWriter::ConfigureFilterUsingProfile.**](iconfigasfwriter-configurefilterusingprofile.md) Esta es la única manera de configurar el filtro con un perfil que usa los códecs Windows media audio y vídeo de la serie 9. Los perfiles del sistema para versiones anteriores de estos códecs se pueden agregar mediante el método [**IConfigASFWriter::ConfigureFilterUsingProfileGuid.**](iconfigasfwriter-configurefilterusingprofileguid.md)

## <a name="adding-metadata-qasf"></a>Agregar metadatos (QASF)

Para agregar metadatos a un archivo, llame a **QueryInterface** desde la interfaz **IBaseFilter** en [WM ASF Writer](wm-asf-writer-filter.md) para recuperar la [**interfaz IWMHeaderInfo.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) Una vez que se haya dado un perfil al filtro, use los métodos de interfaz **IWMHeaderInfo** para escribir los metadatos.

## <a name="indexing-a-file-qasf"></a>Indexación de un archivo (QASF)

Wm ASF Writer crea archivos indizados temporalmente de forma predeterminada. Para crear un archivo indizado por marco, use el método [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md) para deshabilitar toda la indexación y, a continuación, cree el archivo. Cuando haya finalizado, use el SDK Windows Media Format directamente para crear un índice basado en fotogramas para el archivo.

## <a name="performing-two-pass-encoding-qasf"></a>Realizar Two-Pass codificación (QASF)

La codificación de dos pases solo se admite Windows códecs multimedia de la versión 8 y posteriores. Coloque el escritor de ASF wm en modo de preprocesamiento llamando a [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) y especificando AM CONFIGASFWRITER PARAM MULTIPASS en el parámetro dwParam y TRUE en el \_ \_ parámetro \_ *dwParam1.*  

A continuación, ejecute el gráfico de filtro. Cuando se realizan todos los pases de preprocesamiento (normalmente solo se realizará un paso de preprocesamiento), la aplicación recibirá un evento **\_ EC PREPROCESS \_ COMPLETE** del filtro. Cuando se reciba este evento, use **IMediaSeeking::SetPositions** para restablecer el puntero de secuencia al principio y vuelva a ejecutar el gráfico de filtros. Después del último paso (normalmente el segundo paso), la aplicación recibirá un evento **EC \_ COMPLETE** para indicar que el proceso de codificación se ha completado. Si se cancela un paso de preprocesamiento antes de recibir el evento **\_ EC PREPROCESS \_ COMPLETE,** llame a [**IConfigAsfWriter2::ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) para restablecer el filtro antes de intentar otra ejecución de preprocesamiento.

Solo es necesario llamar a **IConfigAsfWriter::SetParam**(AM \_ CONFIGASFWRITER \_ PARAM \_ MULTIPASS, **FALSE**) si desea dejar completamente el filtro fuera del modo de preprocesamiento.

> [!IMPORTANT]
> Es responsabilidad de la aplicación habilitar el modo de preprocesamiento en función del perfil que se usará para la codificación. Algunos perfiles requieren codificación de dos pases; Si intenta codificar un archivo con este tipo de perfil y no establece AM CONFIGASFWRITER PARAM MULTIPASS en TRUE, se producirá un \_ \_ error \_  \_ USERABORT de EC. Para obtener más información sobre cómo determinar si un perfil determinado requiere codificación de dos pasadas, vea Using [Two-Pass Encoding](using-two-pass-encoding.md) or Writing Variable Bit [Rate Secuencias](writing-variable-bit-rate-streams.md).

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a>Obtener y establecer propiedades de búfer en tiempo de ejecución (QASF)

En algunos escenarios, por ejemplo, si desea forzar la inserción de fotogramas clave al escribir un archivo, es posible que una aplicación necesite obtener o establecer información sobre un búfer de Windows Media en tiempo de ejecución. Los filtros [Lector de ASF](wm-asf-reader-filter.md) de WM y Escritor [de ASF](wm-asf-writer-filter.md) de WM admiten un mecanismo de devolución de llamada que permite que una aplicación acceda a la [**interfaz INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) en cada búfer multimedia individual durante la lectura de archivos o la escritura de archivos. Las aplicaciones pueden usar esta interfaz para designar ejemplos específicos como fotogramas clave, o puntos [*limpios,*](wmformat-glossary.md)para establecer códigos de tiempo SMPTE, especificar la configuración de intercalación o agregar cualquier tipo de datos privados a una secuencia.

Use la [**interfaz IAMWMBufferPass para registrarse**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) para las devoluciones de llamada desde el pin que está controlando la secuencia de vídeo. Cuando el pin llame al método [**IAMWMBufferPassCallback::Notify,**](iamwmbufferpasscallback-notify.md) examine las marcas de tiempo en el búfer y, si procede, llame a [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para establecer la propiedad **\_ SampleExtensionGUID \_ OutputCleanPoint** de WM en **TRUE.**

## <a name="non-square-pixel-support-qasf"></a>Compatibilidad con píxeles no cuadrados (QASF)

WM ASF Writer se conecta a un filtro ascendente, como el descodificador DV, que genera información de relación de aspecto de píxeles. Wm ASF Writer escribirá esta información como extensiones de unidad de datos para cada ejemplo del archivo.

Cuando el lector de ASF wm encuentra información de relación de aspecto de píxeles en el encabezado de archivo o en las extensiones de unidad de datos para los ejemplos, ofrecerá un tipo de medio **VIDEOINFOHEADER2** como primera opción en su pin de salida. Los **miembros dwPictAspectRatioX** y **dwPictAspectRatioY** de la estructura, que describen la relación de aspecto del rectángulo de vídeo, se ajustarán correctamente para tener en cuenta la relación de aspecto de píxeles.

## <a name="maintaining-interlaced-format"></a>Mantener el formato entrelazado

Si captura vídeo entrelazado de un televisor o una cámara DV, puede conservar el vídeo original como campos independientes si espera que el archivo codificado se reenvía a un televisor u otro dispositivo de pantalla entrelazado. (Los monitores de equipo son dispositivos de examen progresiva). Si desinterlace un vídeo y, a continuación, lo vuelve a interpretar para su reproducción en un televisor, se incurrirá en alguna pérdida de datos. En un archivo ASF, la información entrelazada se almacena como extensiones de unidad de datos que la aplicación aplica a cada ejemplo mediante el método **IAMWMBufferPassCallback** descrito anteriormente. Para codificar un archivo que conserve la configuración de intercalación original, siga estos pasos:

-   Implemente una clase que **admita IAMWMBufferPassCallback** y escriba una función Notify que establece las marcas de interlace para cada ejemplo. Wm ASF Writer llamará a esta función antes de que procese cada ejemplo.


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   Establezca las extensiones de unidad de datos en el perfil antes de pasar el perfil al filtro.


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   Después de configurar el filtro con el perfil, obtenga la interfaz **IWMWriterAdvanced2** de WM ASF Writer y llame al **método SetInputSettings.**

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
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



 

 