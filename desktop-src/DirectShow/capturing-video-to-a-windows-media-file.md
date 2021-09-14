---
description: Capturar vídeo en un archivo Windows multimedia
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Capturar vídeo en un archivo Windows multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361440"
---
# <a name="capturing-video-to-a-windows-media-file"></a>Capturar vídeo en un archivo Windows multimedia

Para capturar vídeo y codificarlo en un archivo Windows Media Video (WMV), conecte el pin de captura al filtro [WM ASF Writer,](wm-asf-writer-filter.md) como se muestra en el diagrama siguiente.

![Gráfico de captura de windows media](images/vidcap03.png)

La manera más fácil de compilar este gráfico es especificando MEDIASUBTYPE Asf en el método \_ [**ICaptureGraphBuilder2::SetOutputFileName:**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename)


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



El valor MEDIASUBTYPE Asf indica a Capture Graph Builder que use el filtro \_ WM ASF Writer como receptor de archivos. Capture Graph Builder crea el filtro, lo agrega al gráfico y llama a [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) para establecer el nombre del archivo de salida. Devuelve un puntero al filtro como parámetro saliente (


```
pASFWriter
```



en el ejemplo anterior).

Use la [**interfaz IConfigAsfWriter en**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) WM ASF Writer para establecer el Windows media. Debe hacerlo antes de conectar los pines en WM ASF Writer.


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



Para obtener más información sobre cómo establecer el perfil, vea [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).

Llame [**a ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar el filtro de captura a ASF Writer:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



Cada pin de entrada del filtro WM ASF Writer corresponde a una secuencia del perfil Windows media. Debe conectar cada pin para que el contenido del archivo coincida con el perfil.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capturar vídeo en un archivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



