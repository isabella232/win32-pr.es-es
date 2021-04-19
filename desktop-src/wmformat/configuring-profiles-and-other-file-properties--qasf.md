---
title: Configuración de perfiles y otras propiedades de archivo (QASF)
description: Configuración de perfiles y otras propiedades de archivo (QASF)
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- Windows Media Format SDK, configurar perfiles (QASF)
- SDK de Windows Media Format, configurar las propiedades de archivo (QASF)
- SDK de Windows Media Format, metadatos (QASF)
- Advanced Systems Format (ASF), configurar perfiles (QASF)
- ASF (formato de sistemas avanzados), configurar perfiles (QASF)
- Advanced Systems Format (ASF), configurar las propiedades de archivo (QASF)
- ASF (formato de sistemas avanzados), configurar las propiedades de archivo (QASF)
- Advanced Systems Format (ASF), metadatos (QASF)
- ASF (formato de sistemas avanzados), metadatos (QASF)
- SDK de Windows Media Format, QASF
- Advanced Systems Format (ASF), QASF
- ASF (formato de sistemas avanzados), QASF
- metadatos, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488031"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a>Configuración de perfiles y otras propiedades de archivo (QASF)

En los elementos siguientes se describe cómo realizar varias tareas relacionadas con la creación de archivos ASF.

## <a name="creating-a-profile-qasf"></a>Creación de un perfil (QASF)

Para crear un perfil personalizado, use el SDK de Windows Media Format directamente para crear un objeto de administrador de perfiles mediante la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) . A continuación, cree el perfil y páselo al escritor de [ASF de WM](wm-asf-writer-filter.md) mediante el método [**IConfigASFWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) . Esta es la única manera de configurar el filtro con un perfil que use los códecs de la serie Windows Media Audio y vídeo 9. Los perfiles de sistema para versiones anteriores de estos códecs se pueden agregar mediante el método [**IConfigASFWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) .

## <a name="adding-metadata-qasf"></a>Agregar metadatos (QASF)

Para agregar metadatos a un archivo, llame a **QueryInterface** desde la interfaz **IBASEFILTER** del [escritor ASF de WM](wm-asf-writer-filter.md) para recuperar la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) . Una vez que se ha dado un perfil al filtro, use los métodos de la interfaz **IWMHeaderInfo** para escribir los metadatos.

## <a name="indexing-a-file-qasf"></a>Indexación de un archivo (QASF)

De manera predeterminada, el escritor ASF de WM crea archivos indizados de forma temporal. Para crear un archivo indexado mediante Marcos, use el método [**IConfigAsfWriter:: SetIndexMode**](iconfigasfwriter-setindexmode.md) para deshabilitar toda la indexación y, a continuación, cree el archivo. Cuando haya finalizado, use el SDK de Windows Media Format directamente para crear un índice basado en marco para el archivo.

## <a name="performing-two-pass-encoding-qasf"></a>Realización de la codificación de Two-Pass (QASF)

La codificación de dos pasos solo se admite en códecs de Windows Media de la versión 8 y posteriores. Coloque el escritor ASF de WM en modo de preprocesamiento llamando a [**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md) y especificando AM \_ CONFIGASFWRITER \_ param \_ Multipass en el parámetro *DwParam* y **true** en el parámetro *dwParam1* .

A continuación, ejecute el gráfico de filtro. Cuando se realizan todos los pasos de preprocesamiento (normalmente solo se realizará un paso de preprocesamiento), la aplicación recibirá un evento de **\_ \_ finalización de preprocesamiento de EC** del filtro. Cuando se reciba este evento, use **IMediaSeeking:: SetPositions** para restablecer el puntero de secuencia de nuevo al principio y vuelva a ejecutar el gráfico de filtro. Después del último paso (normalmente el segundo paso), la aplicación recibirá un evento de **\_ finalización de EC** para indicar que se ha completado el proceso de codificación. Si se cancela un paso de preprocesamiento antes de que se reciba el evento de **\_ \_ finalización** previa al preprocesamiento, llame a [**IConfigAsfWriter2:: ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) para restablecer el filtro antes de intentar otra ejecución de preprocesamiento.

Solo es necesario llamar a **IConfigAsfWriter:: SetParam**(AM \_ CONFIGASFWRITER \_ param \_ Multipass, **false**) Si desea poner el filtro fuera del modo de preprocesamiento por completo.

> [!IMPORTANT]
> Es responsabilidad de la aplicación habilitar el modo de preprocesamiento según el perfil que se usará para la codificación. Algunos perfiles requieren codificación de dos pasos; Si intenta codificar un archivo con este tipo de perfil y no establece AM \_ CONFIGASFWRITER \_ param \_ Multipass en **true**, se producirá un error de USERABORT de EC \_ . Para obtener más información sobre cómo determinar si un perfil determinado requiere codificación de dos pasos, vea [usar la codificación de Two-Pass](using-two-pass-encoding.md) o [escribir secuencias de velocidad de bits variable](writing-variable-bit-rate-streams.md).

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a>Obtener y establecer propiedades de búfer en tiempo de ejecución (QASF)

En algunos escenarios, por ejemplo, si desea forzar la inserción de fotogramas clave al escribir un archivo, es posible que una aplicación necesite obtener o establecer información sobre un búfer de Windows Media en tiempo de ejecución. Los filtros del [lector ASF de WM](wm-asf-reader-filter.md) y del [escritor ASF de WM](wm-asf-writer-filter.md) admiten un mecanismo de devolución de llamada que permite a una aplicación tener acceso a la interfaz [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) en cada búfer multimedia individual durante la lectura o escritura de archivos. Las aplicaciones pueden usar esta interfaz para designar ejemplos específicos como fotogramas clave, o [*cleanpoints*](wmformat-glossary.md), para establecer códigos de tiempo de SMPTE, para especificar la configuración de entrelazado o para agregar cualquier tipo de datos privados a un flujo.

Use la interfaz [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) para registrar las devoluciones de llamada del PIN que está controlando la secuencia de vídeo. Cuando el PIN llama al método [**IAMWMBufferPassCallback:: Notify**](iamwmbufferpasscallback-notify.md) , examine las marcas de tiempo en el búfer y, si es necesario, llame a [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para establecer la propiedad de **WM \_ SampleExtensionGUID \_ OutputCleanPoint** en el búfer en **true**.

## <a name="non-square-pixel-support-qasf"></a>Compatibilidad con píxeles no cuadrados (QASF)

El escritor ASF de WM se conecta a un filtro de nivel superior, como el descodificador DV, que genera información de relación de aspecto de píxeles. El escritor ASF de WM escribirá esta información como extensiones de unidad de datos para cada muestra del archivo.

Cuando el lector ASF de WM encuentra información de relación de aspecto de píxeles en el encabezado de archivo o en las extensiones de unidad de datos para los ejemplos, ofrecerá un tipo de medio **VIDEOINFOHEADER2** como primera opción en el PIN de salida. Los miembros **dwPictAspectRatioX** y **dwPictAspectRatioY** de la estructura, que describen la relación de aspecto del rectángulo de vídeo, se ajustarán correctamente para tener en cuenta la relación de aspecto de píxeles.

## <a name="maintaining-interlaced-format"></a>Mantener el formato entrelazado

Si captura vídeo entrelazado de una cámara de televisión o DV, es posible que desee conservar el vídeo original como campos independientes si espera que el archivo codificado se reproduzca en un televisor u otro dispositivo de pantalla entrelazada. (Los monitores de equipos son dispositivos de digitalización progresiva). Si desentrelaza un vídeo y, a continuación, lo reentrelaza para su reproducción en un televisor, se producirá una pérdida de datos. En un archivo ASF, la información de entrelazado se almacena como extensiones de unidad de datos que la aplicación aplica a cada ejemplo mediante el método **IAMWMBufferPassCallback** descrito anteriormente. Para codificar un archivo que conserva la configuración de entrelazado original, siga estos pasos:

-   Implemente una clase que admita **IAMWMBufferPassCallback** y escriba una función Notify que establezca las marcas de entrelazado para cada ejemplo. El escritor ASF de WM llamará a esta función antes de procesar cada ejemplo.


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   Establezca las extensiones de unidad de datos en el perfil antes de pasar el perfil al filtro.


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   Después de configurar el filtro con el perfil, obtenga la interfaz **IWMWriterAdvanced2** del escritor ASF de WM y llame al método **SetInputSettings** .

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



 

 