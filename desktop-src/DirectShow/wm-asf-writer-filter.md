---
description: Filtro de escritor ASF de WM
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: Filtro de escritor ASF de WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672996124c88632228fff3a84525c9d47f2276b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155304"
---
# <a name="wm-asf-writer-filter-directshow"></a>Filtro de escritor ASF de WM (DirectShow)

El escritor ASF de WM es un filtro de contenedor para el objeto de escritor que se proporciona con el SDK de Windows Media™ Format. El filtro acepta un número variable de flujos de entrada y crea un archivo de formato de sistema avanzado (ASF). El filtro controla toda la compresión y multiplexación (aunque se puede omitir el mecanismo de compresión). Puede usar el escritor ASF de WM en varios escenarios, como la captura Audio-Video de vídeo digital (DV), la recompresión de audio y la conversión de archivos multimedia intercalados (AVI) o MPEG para la transmisión por secuencias de la red. Este filtro proporciona la única manera de crear archivos de Microsoft® Windows Media™ Audio y Windows Media Video en Microsoft DirectShow.

Para obtener más información, vea [crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md).



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter), [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPersistStream**, **IServiceProvider**, **ISpecifyPropertyPages** además, el filtro expone las siguientes interfaces del SDK de Windows Media Format: **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**<br/> |
| Tipos de medios de anclaje de entrada                    | Depende del perfil ASF. Normalmente, los tipos de audio y vídeo sin comprimir, aunque el filtro aceptará tipos comprimidos si coinciden con el perfil ASF.                                                                                                                                                                                                                                                                                                                                             |
| Interfaces de PIN de entrada                     | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), **IServiceProvider** además, el PIN expone la siguiente interfaz del SDK de Windows Media Format: **IWMStreamConfig2** (a través de **IServiceProvider**)<br/>                                                                                                                                                                                 |
| Tipos de medios de anclaje de salida                   | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces de clavija de salida                    | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Identificador CLSID                             | CLSID \_ WMAsfWriter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CLSID de la página de propiedades                      | CLSID \_ AsfWriterProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Executable                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Fundament](merit.md)                       | MÉRITO \_ \_ no se \_ usa                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Categoría de filtro](filter-categories.md) | No especificado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Observaciones

El filtro requiere el kit de desarrollo de software (SDK) de Windows Media Format y sus dependencias subyacentes.

Número de clavijas de entrada en el filtro según el perfil o el identificador de Perfil de la secuencia ASF.

Los pin de entrada admiten un método de la interfaz **IAMStreamConfig** : [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Todos los demás métodos devuelven E \_ NOTIMPL. Llame al método **GetFormat** para consultar el formato de compresión de destino del PIN, definido por el perfil ASF actual. Use la interfaz [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) para establecer el perfil.

Puede usar la interfaz **IServiceProvider** del filtro para obtener un puntero a la interfaz **IWMWriterAdvanced2** , que se define en el SDK de Windows Media Format. Puede usar la interfaz **IWMWriterAdvanced2** para controlar el desentrelazado de vídeo cuando el vídeo de origen está entrelazado. Para establecer el modo de desentrelazado, llame a **IWMWriterAdvanced2:: SetInputSetting**. Para el parámetro *dwInputNum* , use el índice de base cero del PIN de entrada de vídeo, tal y como lo enumera la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .

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



Las aplicaciones no deben usar ninguno de los métodos **IWMWriterAdvanced** que hereda la interfaz **IWMWriterAdvanced2** . La llamada a cualquiera de estos métodos podría interere con la operación del filtro.

El único modo de escritura de archivos admitido por este filtro es la \_ sobrescritura de archivos AM \_ . Vea [**IFileSinkFilter2:: GetMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode).

Cuando el tiempo de ejecución del SDK de Windows Media Format envía \_ mensajes de estado WMT al filtro del escritor ASF de WM, el filtro los reenvía como eventos de [**\_ \_ evento WMT de EC**](ec-wmt-event.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




