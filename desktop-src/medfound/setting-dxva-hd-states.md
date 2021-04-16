---
description: .
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Configuración de los Estados de la HD de DXVA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e539796aa5d3997b35739e75c80b438a7b5da50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715490"
---
# <a name="setting-dxva-hd-states"></a>Configuración de los Estados de la HD de DXVA

Durante el procesamiento de vídeo, el dispositivo Microsoft DirectX video Acceleration High Definition (DXVA-HD) mantiene un estado persistente de un fotograma a otro. Cada Estado tiene un valor predeterminado documentado. Después de configurar el dispositivo, establezca los Estados que desee cambiar con respecto a sus valores predeterminados. Antes de procesar cada fotograma, actualice los Estados que deben cambiar.

> [!Note]  
> Este diseño es distinto de DXVA-VP. En DXVA-VP, la aplicación debe especificar todos los parámetros VP con cada fotograma.

 

Los Estados de los dispositivos se dividen en dos categorías:

-   Los Estados de *secuencia* aplican cada flujo de entrada por separado. Puede aplicar diferentes configuraciones a cada flujo.
-   Los Estados de *blit* se aplican globalmente a todo el procesamiento de vídeo.

Se definen los siguientes Estados de flujo.



| Estado de la secuencia                                   | Descripción                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **DXVAHD \_ Estado de flujo de \_ \_ D3DFORMAT**           | Formato de vídeo de entrada.                                                                                             |
| **\_formato de \_ marco de estado de secuencia de DXVAHD \_ \_**       | Entrelaza.                                                                                                    |
| **\_espacio de \_ colores de entrada de estado de secuencia de \_ \_ DXVAHD \_** | Espacio de colores de entrada. Este estado especifica el intervalo de color RGB y la matriz de transferencia YCbCr para el flujo de entrada. |
| **\_velocidad de \_ salida de estado de flujo de DXVAHD \_ \_**        | Velocidad de fotogramas de salida. Este estado controla la conversión de velocidad de fotogramas.                                                   |
| **\_rectángulo de \_ origen de estado de flujo de DXVAHD \_ \_**        | Rectángulo de origen.                                                                                               |
| **DXVAHD \_ \_ rectángulo de \_ destino de estado de secuencia \_**   | Rectángulo de destino.                                                                                          |
| **DXVAHD \_ Estado de flujo \_ \_ alfa**               | Alfa plana.                                                                                                   |
| **DXVAHD \_ \_ paleta de estado de flujo \_**             | Paleta de colores. Este estado se aplica solo a los formatos de entrada de paleta.                                             |
| **\_clave de \_ luminancia de estado de flujo de DXVAHD \_ \_**           | Clave de luminancia.                                                                                                       |
| **\_relación de \_ aspecto de estado de flujo de DXVAHD \_ \_**       | Relación de aspecto de píxeles.                                                                                             |
| **Filtro de estado de secuencia de DXVAHD \_ \_ \_ \_ xxxx**        | Configuración del filtro de imágenes. El controlador puede admitir brillo, contraste y otros filtros de imagen.                    |



 

Se definen los siguientes Estados de blit:



| Estado de blit                                   | Descripción                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| **\_rectángulo de \_ destino de estado \_ \_ de DXVAHD BLT**         | Rectángulo de destino.                                                            |
| **\_color de \_ fondo de estado \_ \_ de DXVAHD BLT**    | Color de fondo.                                                            |
| **\_espacio de \_ colores de salida de estado \_ \_ de DXVAHD BLT \_** | Espacio de colores de salida.                                                          |
| **DXVAHD \_ BLT \_ State \_ alfa \_ Fill**          | Modo de relleno alfa.                                                             |
| **DXVAHD \_ BLT \_ State \_ CONSTRICTION**         | Constriction. Este estado controla si el dispositivo downsamples la salida. |



 

Para establecer un estado de flujo, llame al método [**IDXVAHD de \_ videoprocesador:: SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) . Para establecer un estado de Blit, llame al método [**IDXVAHD de \_ videoprocesador:: SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) . En ambos métodos, un valor de enumeración especifica el estado que se va a establecer. Los datos de estado se proporcionan mediante una estructura de datos específica del estado, que la aplicación convierte en un tipo **void \*** .

En el ejemplo de código siguiente se establece el formato de entrada y el rectángulo de destino para la secuencia 0, y se establece el color de fondo en negro.


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



