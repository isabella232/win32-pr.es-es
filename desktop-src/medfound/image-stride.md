---
description: Intervalo de imagen
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: Intervalo de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813c0f3d99297758761bdfb5973fc2b16e3339f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568110"
---
# <a name="image-stride"></a>Intervalo de imagen

Cuando una imagen de vídeo se almacena en memoria, el búfer de memoria podría contener bytes de relleno adicionales después de cada fila de píxeles. Los bytes de relleno afectan a cómo se almacena la imagen en memoria, pero no afectan al modo en que se muestra la imagen.

*STRIDE* es el número de bytes de una fila de píxeles en memoria hasta la siguiente fila de píxeles de la memoria. STRIDE también se denomina *paso*. Si los bytes de relleno están presentes, el intervalo es más ancho que el ancho de la imagen, como se muestra en la siguiente ilustración.

![diagrama que muestra una imagen más el relleno.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

Dos búferes que contienen fotogramas de vídeo con dimensiones iguales pueden tener dos progresos diferentes. Si procesa una imagen de vídeo, debe tener en cuenta el intervalo.

Además, hay dos formas de organizar una imagen en memoria. En una imagen de *arriba abajo* , la fila superior de píxeles de la imagen aparece en primer lugar en la memoria. En una imagen de *abajo arriba* , la última fila de píxeles aparece en primer lugar en la memoria. En la ilustración siguiente se muestra la diferencia entre una imagen de arriba abajo y una imagen de arriba abajo.

![diagrama que muestra imágenes de arriba abajo e inferior.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

Una imagen de orden ascendente tiene un intervalo negativo, porque STRIDE se define como el número de bytes necesario para bajar una fila de píxeles, con respecto a la imagen mostrada. Las imágenes YUV siempre deben ser de arriba abajo y cualquier imagen que esté contenida en una superficie de Direct3D debe ser de arriba abajo. Las imágenes RGB en la memoria del sistema suelen estar en orden ascendente.

En particular, las transformaciones de vídeo necesitan controlar los búferes con los progresos no coincidentes, ya que el búfer de entrada podría no coincidir con el búfer de salida. Por ejemplo, supongamos que desea convertir una imagen de origen y escribir el resultado en una imagen de destino. Suponga que ambas imágenes tienen el mismo ancho y alto, pero puede que no tengan el mismo formato de píxel o el mismo intervalo de imagen.

En el ejemplo de código siguiente se muestra un enfoque generalizado para escribir este tipo de función. No se trata de un ejemplo de trabajo completo, porque abstrae muchos de los detalles específicos.


```C++
void ProcessVideoImage(
    BYTE*       pDestScanLine0,     
    LONG        lDestStride,        
    const BYTE* pSrcScanLine0,      
    LONG        lSrcStride,         
    DWORD       dwWidthInPixels,     
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        SOURCE_PIXEL_TYPE *pSrcPixel = (SOURCE_PIXEL_TYPE*)pDestScanLine0;
        DEST_PIXEL_TYPE *pDestPixel = (DEST_PIXEL_TYPE*)pSrcScanLine0;

        for (DWORD x = 0; x < dwWidthInPixels; x +=2)
        {
            pDestPixel[x] = TransformPixelValue(pSrcPixel[x]);
        }
        pDestScanLine0 += lDestStride;
        pSrcScanLine0 += lSrcStride;
    }
}
```



Esta función toma seis parámetros:

-   Un puntero al inicio de la línea de recorrido 0 en la imagen de destino.
-   El paso de la imagen de destino.
-   Un puntero al inicio de la línea de recorrido 0 en la imagen de origen.
-   El paso de la imagen de origen.
-   Ancho de la imagen en píxeles.
-   Alto de la imagen en píxeles.

La idea general es procesar una fila cada vez, iterando por cada píxel de la fila. Supongamos que el tipo \_ \_ de píxel de origen y el \_ tipo de píxel de destino \_ son estructuras que representan el diseño de píxeles para las imágenes de origen y de destino, respectivamente. (Por ejemplo, RGB de 32 bits usa la estructura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) . No todos los formatos de píxel tienen una estructura predefinida). Convertir el puntero de matriz al tipo de estructura le permite tener acceso a los componentes RGB o YUV de cada píxel. Al principio de cada fila, la función almacena un puntero a la fila. Al final de la fila, incrementa el puntero en el ancho del intervalo de la imagen, lo que hace avanzar el puntero a la fila siguiente.

En este ejemplo se llama a una función hipotética denominada TransformPixelValue para cada píxel. Puede ser cualquier función que calcule un píxel de destino de un píxel de origen. Por supuesto, los detalles exactos dependerán de la tarea determinada. Por ejemplo, si tiene un formato YUV plano, debe tener acceso a los planos de croma independientemente del plano de luminancia; con vídeo entrelazado, es posible que tenga que procesar los campos por separado. etc.

Para dar un ejemplo más concreto, el código siguiente convierte una imagen RGB de 32 bits en una imagen AYUV. Se tiene acceso a los píxeles RGB mediante una estructura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) y se tiene acceso a los píxeles de AYUV mediante una estructura de estructura [**DXVA2 \_ AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) .


```C++
//-------------------------------------------------------------------
// Name: RGB32_To_AYUV
// Description: Converts an image from RGB32 to AYUV
//-------------------------------------------------------------------
void RGB32_To_AYUV(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD             *pSrcPixel = (RGBQUAD*)pSrc;
        DXVA2_AYUVSample8   *pDestPixel = (DXVA2_AYUVSample8*)pDest;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestPixel[x].Alpha = 0x80;
            pDestPixel[x].Y = RGBtoY(pSrcPixel[x]);   
            pDestPixel[x].Cb = RGBtoU(pSrcPixel[x]);   
            pDestPixel[x].Cr = RGBtoV(pSrcPixel[x]);   
        }
        pDest += lDestStride;
        pSrc += lSrcStride;
    }
}
```



En el ejemplo siguiente se convierte una imagen RGB de 32 bits en una imagen YV12. En este ejemplo se muestra cómo controlar un formato YUV plano. (YV12 es un formato plano 4:2:0). En este ejemplo, la función mantiene tres punteros independientes para los tres planos de la imagen de destino. Sin embargo, el enfoque básico es el mismo que el ejemplo anterior.


```C++
void RGB32_To_YV12(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    assert(dwWidthInPixels % 2 == 0);
    assert(dwHeightInPixels % 2 == 0);

    const BYTE *pSrcRow = pSrc;
    
    BYTE *pDestY = pDest;

    // Calculate the offsets for the V and U planes.

    // In YV12, each chroma plane has half the stride and half the height  
    // as the Y plane.
    BYTE *pDestV = pDest + (lDestStride * dwHeightInPixels);
    BYTE *pDestU = pDest + 
                   (lDestStride * dwHeightInPixels) + 
                   ((lDestStride * dwHeightInPixels) / 4);

    // Convert the Y plane.
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestY[x] = RGBtoY(pSrcPixel[x]);    // Y0
        }
        pDestY += lDestStride;
        pSrcRow += lSrcStride;
    }

    // Convert the V and U planes.

    // YV12 is a 4:2:0 format, so each chroma sample is derived from four 
    // RGB pixels.
    pSrcRow = pSrc;
    for (DWORD y = 0; y < dwHeightInPixels; y += 2)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        RGBQUAD *pNextSrcRow = (RGBQUAD*)(pSrcRow + lSrcStride);

        BYTE *pbV = pDestV;
        BYTE *pbU = pDestU;

        for (DWORD x = 0; x < dwWidthInPixels; x += 2)
        {
            // Use a simple average to downsample the chroma.

            *pbV++ = ( RGBtoV(pSrcPixel[x]) +
                       RGBtoV(pSrcPixel[x + 1]) +       
                       RGBtoV(pNextSrcRow[x]) +         
                       RGBtoV(pNextSrcRow[x + 1]) ) / 4;        

            *pbU++ = ( RGBtoU(pSrcPixel[x]) +
                       RGBtoU(pSrcPixel[x + 1]) +       
                       RGBtoU(pNextSrcRow[x]) +         
                       RGBtoU(pNextSrcRow[x + 1]) ) / 4;    
        }
        pDestV += lDestStride / 2;
        pDestU += lDestStride / 2;
        
        // Skip two lines on the source image.
        pSrcRow += (lSrcStride * 2);
    }
}
```



En todos estos ejemplos, se supone que la aplicación ya ha determinado el intervalo de la imagen. A veces, puede obtener esta información del búfer de medios. De lo contrario, debe calcularlo en función del formato de vídeo. Para obtener más información sobre cómo calcular el intervalo de imagen y trabajar con búferes multimedia para vídeo, consulte [búferes de vídeo sin comprimir](uncompressed-video-buffers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 
