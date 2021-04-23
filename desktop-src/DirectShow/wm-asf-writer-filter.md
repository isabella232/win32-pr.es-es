---
description: Filtro de escritor de ASF de WM
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: Filtro wm asf writer (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf09a99673b07e88198fd57b95a766ce821eb02
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909283"
---
# <a name="wm-asf-writer-filter-directshow"></a>Filtro wm asf writer (DirectShow)

WM ASF Writer es un filtro contenedor para el objeto de escritor proporcionado con el SDK de Windows Media™ Format. El filtro acepta un número variable de flujos de entrada y crea un archivo de formato de sistemas avanzados (ASF). El filtro controla toda la compresión y la multiplexación (aunque se puede omitir el mecanismo de compresión). Puede usar WM ASF Writer en varios escenarios, como la captura de vídeo digital (DV), la recom Audio-Video presión de audio y la conversión de archivos multimedia intercalados (AVI) o MPEG para streaming de red. Este filtro proporciona la única manera de crear archivos ® Audio y ™ De Windows Media Windows Media Video en Microsoft DirectShow.

Para obtener más información, vea [Crear archivos ASF en DirectShow.](creating-asf-files-in-directshow.md)



| Etiqueta | Value |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter), [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPersistStream**, **IServiceProvider**, **ISpecifyPropertyPages** Además, el filtro expone las siguientes interfaces del SDK de Windows Media Format: **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**<br/> |
| Tipos de medios de pin de entrada                    | Depende del perfil de ASF. Normalmente, los tipos de audio y vídeo no se comprimen, aunque el filtro aceptará tipos comprimidos si coinciden con el perfil de ASF.                                                                                                                                                                                                                                                                                                                                             |
| Interfaces de pin de entrada                     | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMWMBufferPass,**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) **IServiceProvider** Además, el pin expone la siguiente interfaz del SDK de Windows Media Format: **IWMStreamConfig2** (a través de **IServiceProvider**)<br/>                                                                                                                                                                                 |
| Tipos de medios de pin de salida                   | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces de pin de salida                    | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Filtrar CLSID                             | CLSID \_ WMAsfWriter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CLSID de la página de propiedades                      | CLSID \_ AsfWriterProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Executable                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Mérito](merit.md)                       | NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Categoría de filtro](filter-categories.md) | No especificado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Comentarios

El filtro requiere el kit Windows Media Format desarrollo de software (SDK) y sus dependencias subyacentes.

Número de pines de entrada en el filtro en función del identificador de perfil o perfil de la secuencia de ASF.

Las clavijas de entrada admiten un método de la **interfaz IAMStreamConfig:** [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Todos los demás métodos devuelven E \_ NOTIMPL. Llame al **método GetFormat** para consultar el formato de compresión de destino del pin, que se define mediante el perfil de ASF actual. Use la [**interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) para establecer el perfil.

Puede usar la interfaz **IServiceProvider** del filtro para obtener un puntero a la interfaz **IWMWriterAdvanced2,** que se define en Windows Media Format SDK. Puede usar la **interfaz IWMWriterAdvanced2** para controlar el desinterlazado de vídeo cuando el vídeo de origen está entrelazado. Para establecer el modo de desenlace, llame a **IWMWriterAdvanced2::SetInputSetting**. Para el *parámetro dwInputNum,* use el índice de base cero del pin de entrada de vídeo, como se enumera en la [**interfaz IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins)

En el ejemplo siguiente se muestra cómo consultar esta interfaz:


```C++
// Assume that pAsfWriter is a valid IBaseFilter pointer.
IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = pAsfWriter->QueryInterface(
    IID_IServiceProvider, 
    (void**)&pProvider
    );
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(
        IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, 
        (void**)&pWMWA2
        );
    pProvider->Release();
    if (SUCCEEDED(hr))
    {
        // Use pWMWA2. (Not shown.)
        pWMWA2->Release();
    }
}
```



Las aplicaciones no deben usar ninguno de los métodos **IWMWriterAdvanced** que hereda la interfaz **IWMWriterAdvanced2.** Llamar a cualquiera de estos métodos podría intererer con la operación del filtro.

El único modo de escritura de archivos admitido por este filtro es AM \_ FILE \_ OVERWRITE. Vea [**IFileSinkFilter2::GetMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode).

Cuando el runtime Windows Media Format SDK envía mensajes WMT STATUS al filtro WM ASF Writer, el filtro los \_ reenvía como eventos [**\_ EC WMT \_ EVENT.**](ec-wmt-event.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




