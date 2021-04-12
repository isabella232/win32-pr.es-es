---
title: Generar gráficos de filtro en aplicaciones de DRM-Enabled
description: Generar gráficos de filtro en aplicaciones de DRM-Enabled
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- SDK de Windows Media Format, crear gráficos de filtros
- Windows Media Format SDK, DirectShow
- SDK de Windows Media Format, aplicaciones habilitadas para DRM
- Advanced Systems Format (ASF), generar gráficos de filtros
- ASF (formato de sistemas avanzados), crear gráficos de filtros
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), aplicaciones habilitadas para DRM
- ASF (formato de sistemas avanzados), aplicaciones habilitadas para DRM
- DirectShow, crear gráficos de filtros
- DirectShow, aplicaciones habilitadas para DRM
- Administración de derechos digitales (DRM), DirectShow
- DRM (administración de derechos digitales), DirectShow
- Administración de derechos digitales (DRM), crear gráficos de filtros
- DRM (administración de derechos digitales), crear gráficos de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944037a00c208e1427d3d19aa6c9dc0a352ec5fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358705"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a>Generar gráficos de filtro en aplicaciones de DRM-Enabled

Si la aplicación de DirectShow admite la reproducción de archivos protegidos con DRM, por lo general no debe usar **RenderFile** para crear el gráfico de filtros porque no hay ninguna manera de especificar qué derechos de DRM solicita antes de que se abra el archivo. De forma predeterminada, el lector ASF de WM solicita únicamente los derechos de reproducción. El filtro no se agrega al gráfico y, por lo tanto, no lo pueden detectar las aplicaciones hasta que un archivo se abre correctamente.

Para compilar un gráfico de reproducción habilitado con DRM mediante el [lector ASF de WM](wm-asf-reader-filter.md), debe crear una instancia del filtro mediante **CoCreateInstance**, agregarlo al gráfico de filtros mediante **IGraphBuilder:: addFilter**, configurarlo y, a continuación, representar sus clavijas de salida. Esta técnica se muestra en el ejemplo PlayWndASF. Al compilar el gráfico de esta manera, ya tiene el puntero **IBaseFilter** que se puede usar para llamar a **QueryService** para obtener **IWMDRMWriter**. Sin embargo, esta interfaz no está disponible hasta que el lector ASF de WM crea internamente el objeto lector del SDK de Windows Media Format. La primera oportunidad que tiene la aplicación para establecer derechos DRM es en su \_ controlador de eventos WMT no \_ Rights \_ ex, tal como se muestra en este fragmento de código:


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

[**Características de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Lista de atributos de DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




