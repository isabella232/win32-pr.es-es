---
description: Capturar vídeo en un archivo de Windows Media
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Capturar vídeo en un archivo de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279802"
---
# <a name="capturing-video-to-a-windows-media-file"></a>Capturar vídeo en un archivo de Windows Media

Para capturar vídeo y codificarlo en un archivo Windows Media Video (WMV), conecte el PIN de captura al filtro del [escritor ASF de WM](wm-asf-writer-filter.md) , tal como se muestra en el diagrama siguiente.

![gráfico de captura de Windows Media](images/vidcap03.png)

La forma más sencilla de compilar este grafo es especificar MEDIASUBTYPE \_ ASF en el método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



El valor MEDIASUBTYPE \_ ASF indica al generador de gráficos de captura que use el filtro de escritor ASF de WM como receptor de archivos. El generador de gráficos de captura crea el filtro, lo agrega al gráfico y llama a [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) para establecer el nombre del archivo de salida. Devuelve un puntero al filtro como un parámetro saliente (


```
pASFWriter
```



en el ejemplo anterior).

Use la interfaz [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) en el escritor ASF de WM para establecer el perfil de Windows Media. Debe hacerlo antes de conectar cualquier PIN en el escritor ASF de WM.


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



Para obtener más información acerca de cómo configurar el perfil, vea [crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md).

Llame a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar el filtro de captura al escritor ASF:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



Cada pin de entrada del filtro de escritura ASF de WM corresponde a una secuencia en el perfil de Windows Media. Debe conectar cada pin para que el contenido del archivo coincida con el perfil.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capturar vídeo en un archivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



