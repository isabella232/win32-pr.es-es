---
title: Creación de gráficos de filtro en DRM-Enabled aplicaciones
description: Creación de gráficos de filtro en DRM-Enabled aplicaciones
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- Windows SDK de formato multimedia, creación de gráficos de filtro
- Windows SDK de formato multimedia, DirectShow
- Windows SDK de formato multimedia, aplicaciones habilitadas para DRM
- Formato de sistemas avanzados (ASF), creación de gráficos de filtro
- ASF (formato de sistemas avanzados), creación de gráficos de filtro
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- Formato de sistemas avanzados (ASF), aplicaciones habilitadas para DRM
- ASF (formato de sistemas avanzados), aplicaciones habilitadas para DRM
- DirectShow, crear gráficos de filtro
- DirectShow aplicaciones habilitadas para DRM
- administración de derechos digitales (DRM),DirectShow
- DRM (administración de derechos digitales),DirectShow
- administración de derechos digitales (DRM), creación de gráficos de filtro
- DRM (administración de derechos digitales), creación de gráficos de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e7f411a52c0ce7c42410c7a901787c7f6d9d7089921019639cb3f5e708dff6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447955"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a>Creación de gráficos de filtro en DRM-Enabled aplicaciones

Si la aplicación DirectShow admite la reproducción de archivos protegidos con DRM, por lo general no debe usar **RenderFile** para crear el gráfico de filtros porque no hay ninguna manera de especificar qué derechos DRM está solicitando antes de abrir el archivo. De forma predeterminada, el lector de ASF de WM solo solicita derechos de reproducción. El filtro no se agrega al gráfico y, por lo tanto, las aplicaciones no pueden detectarlo hasta que un archivo se abre correctamente.

Para crear un gráfico de reproducción habilitado para DRM mediante el lector [DE ASF](wm-asf-reader-filter.md)de WM, debe crear una instancia del filtro mediante **CoCreateInstance,** agregarlo al gráfico de filtros mediante **IGraphBuilder::AddFilter,** configurarlo y, a continuación, representar sus pines de salida. Esta técnica se muestra en el ejemplo PlayWndASF. Al compilar el gráfico de esta manera, ya tiene el puntero **IBaseFilter** que se puede usar para llamar a **QueryService** para obtener **IWMDRMWriter**. Sin embargo, esta interfaz no está disponible hasta que el lector de ASF de WM crea internamente Windows objeto de lector del SDK de formato multimedia. La primera oportunidad que tiene la aplicación para establecer derechos DRM es en su controlador de eventos WMT NO RIGHTS EX, como se \_ muestra en este fragmento de \_ \_ código:


```C++
case WMT_NO_RIGHTS_EX:

    IServiceProvider *pServiceProvider;
    IWMDRMReader pWMDRMReader;
    JIF(g_pReader->QueryInterface(IID_IServiceProvider, (void **) &pServiceProvider));
    JIF(pServiceProvider->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader)); 
    SAFE_RELEASE(pServiceProvider);

    // Set the rights we want for this file. These are the actions we 
    // might want to perform on the file. Here we ask for two rights only.
    // In a real application you should enable users to select which 
    // rights they want.
    hr = pWMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
        BYTE*) wszRights, (sizeof(wszRights) / sizeof(wszRights[0])) * 2);
    SAFE_RELEASE(pWMDRMReader);
    if (FAILED(hr))
    {
       Msg(TEXT("SetDRMProperty Failed!  hr=0x%x\n"), hr);
       return hr;
    }
    // Now proceed with license acqusition.
    if( pEventData->pData )
    {
        hr = HandleNoRightsEx(pEventData->hrStatus, 
        (WM_GET_LICENSE_DATA *)pEventData->pData);
    }
    else
    {
         hr = E_FAIL;
    }
    break;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




