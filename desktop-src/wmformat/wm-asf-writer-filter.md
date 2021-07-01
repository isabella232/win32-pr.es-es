---
title: Filtro wm asf writer (Windows Media Format SDK 11)
description: Obtenga información sobre el filtro WM ASF Writer para el SDK Windows Media Format 11. Revise la información del filtro y vea los temas relacionados.
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK,WM ASF Writer
- DirectShow,WM ASF Writer
- Filtros QASF,WM ASF Writer
- WM ASF Writer,about
- Formato de sistemas avanzados (ASF),WM ASF Writer
- ASF (formato de sistemas avanzados),WM ASF Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee013b55455c3100ee23e076b767d70fb3ffda
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119670"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a>Filtro wm asf writer (Windows Media Format SDK 11)

El filtro WM ASF Writer acepta un número variable de flujos de entrada y crea un archivo ASF. El filtro controla toda la compresión y la multiplexación (aunque se puede omitir el mecanismo de compresión). Puede usar el filtro WM ASF Writer en varios escenarios, como la captura de vídeo digital (DV), la re Audio-Video compresión de audio y la conversión de archivos multimedia digitales intercalados (AVI) o MPEG para streaming de red. Este filtro proporciona la única manera de crear archivos Windows Media Audio Microsoft Windows Media Video en DirectShow.

Para obtener más información, vea [Crear archivos ASF en DirectShow.](creating-asf-files-in-directshow.md)

La tabla siguiente contiene información sobre el filtro WM ASF Writer, como las interfaces y los tipos de medios que admite.



| Filtrar información                       |  Tipos                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro      | **IAMFilterMiscFlags,** **IBaseFilter,** **IConfigAsfWriter**, **IFileSinkFilter2,** IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2** |
| Tipos de medios de pin de entrada  | Depende del perfil. Normalmente, los tipos sin comprimir, como audio MEDIATYPE o vídeo MEDIATYPE, aunque se pueden aceptar tipos comprimidos si \_ \_ coinciden con el perfil                                                   |
| Interfaces de pin de entrada   | **IPin,** **IMemInputPin,** **IAMStreamConfig,** **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (a través **de IServiceProvider**)                                                                         |
| Tipos de medios de pin de salida | No aplicable                                                                                                                                                                                                          |
| Interfaces de pin de salida  | No aplicable                                                                                                                                                                                                          |
| Filtrar CLSID           | CLSID \_ WMAsfWriter                                                                                                                                                                                                      |
| CLSID de la página de propiedades    | CLSID \_ WMAsfWriterProperties                                                                                                                                                                                            |
| Executable             | Qasf.dll                                                                                                                                                                                                                |
| Mérito                  | NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.                                                                                                                                                                                                     |
| Categoría de filtro        | No especificado                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Observaciones

El número de pines de entrada en el filtro depende del perfil que se pasa al filtro. Se crea un pin del tipo de medio adecuado para cada secuencia definida en el perfil.

Las clavijas de entrada admiten un método de la **interfaz IAMStreamConfig:** **IAMStreamConfig::GetFormat**. Todos los demás métodos devuelven E \_ NOTIMPL. Llame al **método GetFormat** para consultar el formato de compresión de destino del pin, definido por el perfil actual. Use la [**interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) para establecer el perfil.

La interfaz **IServiceProvider** del filtro permite a las aplicaciones recuperar la interfaz [**IWMWriterAdvanced2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) que se define en Windows Media Format SDK. La **interfaz IWMWriterAdvanced2** controla el desinterlazado de [](wmformat-glossary.md) vídeo y es útil si la entrada es un origen entrelazado, como DV (vídeo digital). Use los **métodos GetInputSetting** **y SetInputSetting** para controlar el desinterlazado. No se recomienda que los clientes usen ninguno de los otros métodos en esta interfaz. Esta interfaz solo se puede obtener después de agregar el filtro al gráfico de filtros. En el ejemplo siguiente se muestra cómo consultar esta interfaz:


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

[**Referencia de QaSF de DirectShow**](directshow-qasf-reference.md)
</dt> </dl>

 

 
