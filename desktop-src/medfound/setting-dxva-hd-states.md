---
description: Configuración de estados DXVA-HD
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Configuración de estados DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91766e3eb10399d908ab361e13db4b94fe07b653
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574792"
---
# <a name="setting-dxva-hd-states"></a>Configuración de estados DXVA-HD

Durante el procesamiento de vídeo, el dispositivo de alta definición de aceleración de vídeo (DXVA-HD) de Microsoft DirectX mantiene un estado persistente de un fotograma a otro. Cada estado tiene un valor predeterminado documentado. Después de configurar el dispositivo, establezca los estados que quiera cambiar de sus valores predeterminados. Antes de procesar cada fotograma, actualice los estados que deben cambiar.

> [!Note]  
> Este diseño difiere de DXVA-VP. En DXVA-VP, la aplicación debe especificar todos los parámetros de VP con cada fotograma.

 

Los estados del dispositivo se divide en dos categorías:

-   *Los estados* de secuencia aplican cada flujo de entrada por separado. Puede aplicar diferentes configuraciones a cada secuencia.
-   *Los estados de Blit* se aplican globalmente a todo el procesamiento de vídeo blit.

Se definen los siguientes estados de secuencia.



| Estado de la secuencia                                   | Descripción                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **DXVAHD \_ STREAM \_ STATE \_ D3DFORMAT**           | Formato de vídeo de entrada.                                                                                             |
| **FORMATO DE MARCO DE \_ ESTADO DE \_ FLUJO \_ DXVAHD \_**       | Entrelazado.                                                                                                    |
| **ESPACIO DE COLOR DE \_ ENTRADA DE ESTADO DE \_ FLUJO \_ \_ DXVAHD \_** | Espacio de color de entrada. Este estado especifica el intervalo de colores RGB y la matriz de transferencia YCbCr para el flujo de entrada. |
| **VELOCIDAD DE SALIDA DEL ESTADO DE FLUJO DXVAHD \_ \_ \_ \_**        | Velocidad de fotogramas de salida. Este estado controla la conversión de velocidad de fotogramas.                                                   |
| **DXVAHD \_ STREAM \_ STATE \_ SOURCE \_ RECT**        | Rectángulo de origen.                                                                                               |
| **DXVAHD \_ STREAM \_ STATE \_ DESTINATION \_ RECT**   | Rectángulo de destino.                                                                                          |
| **DXVAHD \_ STREAM \_ STATE \_ ALPHA**               | Alfa plana.                                                                                                   |
| **PALETA DE ESTADO DE FLUJO DXVAHD \_ \_ \_**             | Paleta de colores. Este estado solo se aplica a los formatos de entrada con limitaciones.                                             |
| **DXVAHD \_ STREAM \_ STATE \_ LUMA \_ KEY**           | Clave Luma.                                                                                                       |
| **RELACIÓN DE ASPECTO DEL ESTADO DEL FLUJO DXVAHD \_ \_ \_ \_**       | Relación de aspecto de píxeles.                                                                                             |
| **DXVAHD \_ STREAM \_ STATE \_ FILTER \_ Xxxx**        | Configuración del filtro de imagen. El controlador puede admitir el brillo, el contraste y otros filtros de imagen.                    |



 

Se definen los siguientes estados de blit:



| Estado de Blit                                   | Descripción                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| **DXVAHD \_ BLT \_ STATE \_ TARGET \_ RECT**         | Rectángulo de destino.                                                            |
| **COLOR DE FONDO DE \_ ESTADO BLT DXVAHD \_ \_ \_**    | Color de fondo.                                                            |
| **ESPACIO DE COLOR DE SALIDA \_ DE ESTADO BLT DXVAHD \_ \_ \_ \_** | Espacio de color de salida.                                                          |
| **RELLENO ALFA DE ESTADO BLT DXVAHD \_ \_ \_ \_**          | Modo de relleno alfa.                                                             |
| **CONSTRICCIÓN DEL \_ ESTADO BLT \_ DE DXVAHD \_**         | Constricción. Este estado controla si el dispositivo reduce la muestra de la salida. |



 

Para establecer un estado de secuencia, llame al [**método IDXVAHD \_ VideoProcessor::SetVideoProcessStreamState.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) Para establecer un estado blit, llame al método [**IDXVAHD \_ VideoProcessor::SetVideoProcessBltState.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) En ambos métodos, un valor de enumeración especifica el estado que se debe establecer. Los datos de estado se entregan mediante una estructura de datos específica del estado, que la aplicación convierte a un **tipo void. \***

En el ejemplo de código siguiente se establece el formato de entrada y el rectángulo de destino para el flujo 0 y el color de fondo en negro.


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

 

 



