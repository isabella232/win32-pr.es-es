---
title: Filtro del escritor ASF de WM (Windows Media Format 11 SDK)
description: Filtro de escritor ASF de WM
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK, WM ASF Writer
- DirectShow, escritor ASF de WM
- Filtros de QASF, escritor ASF de WM
- Escritor ASF de WM, acerca de
- Advanced Systems Format (ASF), WM ASF Writer
- ASF (formato de sistemas avanzados), escritor ASF de WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0de34bcf4b4047673f832d78f40377f98e94d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105685816"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a>Filtro del escritor ASF de WM (Windows Media Format 11 SDK)

El filtro de escritura ASF de WM acepta un número variable de flujos de entrada y crea un archivo ASF. El filtro controla toda la compresión y multiplexación (aunque se puede omitir el mecanismo de compresión). Puede usar el filtro de escritor ASF de WM en varios escenarios, como la captura Audio-Video de vídeo digital (DV), la recompresión de audio y la conversión de archivos multimedia digitales intercalados (AVI) o MPEG para la transmisión por secuencias de la red. Este filtro proporciona la única manera de crear archivos de Microsoft Windows Media Audio y Windows Media Video en DirectShow.

Para obtener más información, vea [crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md).

La tabla siguiente contiene información sobre el filtro del escritor ASF de WM, como las interfaces y los tipos de medios que admite.



|                        |                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro      | **IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2** |
| Tipos de medios de anclaje de entrada  | Depende del perfil. Normalmente tipos sin comprimir como \_ el vídeo de tipo mediatype audio o mediatype \_ , aunque se pueden aceptar tipos comprimidos si coinciden con el perfil                                                   |
| Interfaces de PIN de entrada   | **IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (a través de **IServiceProvider**)                                                                         |
| Tipos de medios de anclaje de salida | No aplicable                                                                                                                                                                                                          |
| Interfaces de clavija de salida  | No aplicable                                                                                                                                                                                                          |
| Identificador CLSID           | CLSID \_ WMAsfWriter                                                                                                                                                                                                      |
| CLSID de la página de propiedades    | CLSID \_ WMAsfWriterProperties                                                                                                                                                                                            |
| Executable             | Qasf.dll                                                                                                                                                                                                                |
| Fundament                  | MÉRITO \_ \_ no se \_ usa                                                                                                                                                                                                     |
| Categoría de filtro        | No especificado                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Observaciones

El número de clavijas de entrada en el filtro depende del perfil que se pasa al filtro. Se crea un PIN del tipo de medio adecuado para cada flujo definido en el perfil.

Los pin de entrada admiten un método de la interfaz **IAMStreamConfig** : **IAMStreamConfig:: GetFormat**. Todos los demás métodos devuelven E \_ NOTIMPL. Llame al método **GetFormat** para consultar el formato de compresión de destino del PIN, definido por el perfil actual. Use la interfaz [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) para establecer el perfil.

La interfaz **IServiceProvider** del filtro permite a las aplicaciones recuperar la interfaz [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , que se define en el SDK de Windows Media Format. La interfaz **IWMWriterAdvanced2** controla el desentrelazado de vídeo y es útil si la entrada es un origen [*entrelazado*](wmformat-glossary.md) , como DV (vídeo digital). Use los métodos **GetInputSetting** y **SetInputSetting** para controlar el desentrelazado. No se recomienda que los clientes usen ninguno de los otros métodos de esta interfaz. Esta interfaz solo se puede obtener una vez que se ha agregado el filtro al gráfico de filtro. En el ejemplo siguiente se muestra cómo consultar esta interfaz:


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de QASF de DirectShow**](directshow-qasf-reference.md)
</dt> </dl>

 

 
