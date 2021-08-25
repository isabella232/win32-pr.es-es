---
description: Image Stride
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: Image Stride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360afb6fdeca4c543957326b041654d75ff17b66db8918e42d781d414e8b7586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958159"
---
# <a name="image-stride"></a>Image Stride

Cuando una imagen de vídeo se almacena en memoria, el búfer de memoria puede contener bytes de relleno adicionales después de cada fila de píxeles. Los bytes de relleno afectan a cómo se almacena la imagen en memoria, pero no afectan a cómo se muestra la imagen.

El *paso es el* número de bytes de una fila de píxeles en memoria a la siguiente fila de píxeles en memoria. Stride también se denomina *pitch*. Si hay bytes de relleno, el paso es más ancho que el ancho de la imagen, como se muestra en la ilustración siguiente.

![diagrama que muestra una imagen más relleno.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

Dos búferes que contienen fotogramas de vídeo con dimensiones iguales pueden tener dos avances diferentes. Si procesa una imagen de vídeo, debe tener en cuenta el paso.

Además, hay dos maneras de organizar una imagen en memoria. En una *imagen de arriba a* abajo, la fila superior de píxeles de la imagen aparece en primer lugar en la memoria. En una *imagen de abajo* hacia arriba, la última fila de píxeles aparece primero en la memoria. En la ilustración siguiente se muestra la diferencia entre una imagen de arriba abajo y una imagen de abajo hacia arriba.

![diagrama que muestra imágenes de arriba abajo y de abajo hacia arriba.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

Una imagen de abajo hacia arriba tiene un paso negativo, ya que se define stride como el número de bytes que se necesitan para bajar una fila de píxeles, en relación con la imagen mostrada. Las imágenes YUV siempre deben estar de arriba abajo y cualquier imagen que esté contenida en una superficie de Direct3D debe estar de arriba abajo. Las imágenes RGB de la memoria del sistema suelen estar de abajo hacia arriba.

En concreto, las transformaciones de vídeo necesitan controlar los búferes con avances no coincidentes, ya que es posible que el búfer de entrada no coincida con el búfer de salida. Por ejemplo, suponga que desea convertir una imagen de origen y escribir el resultado en una imagen de destino. Suponga que ambas imágenes tienen el mismo ancho y alto, pero es posible que no tengan el mismo formato de píxel o el mismo paso de imagen.

En el código de ejemplo siguiente se muestra un enfoque generalizado para escribir este tipo de función. No se trata de un ejemplo completo de trabajo, ya que abstrae muchos de los detalles específicos.


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

-   Puntero al inicio de la línea de examen 0 en la imagen de destino.
-   Paso de la imagen de destino.
-   Puntero al inicio de la línea de examen 0 en la imagen de origen.
-   El paso de la imagen de origen.
-   Ancho de la imagen en píxeles.
-   Alto de la imagen en píxeles.

La idea general es procesar una fila a la vez, iterando por cada píxel de la fila. Supongamos que SOURCE PIXEL TYPE y DEST PIXEL TYPE son estructuras que representan el diseño de píxeles para las imágenes de origen \_ \_ y \_ \_ destino, respectivamente. (Por ejemplo, RGB de 32 bits usa la [**estructura RGBQUAD.**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) No todos los formatos de píxeles tienen una estructura predefinida). Convertir el puntero de matriz al tipo de estructura le permite acceder a los componentes RGB o YUV de cada píxel. Al principio de cada fila, la función almacena un puntero a la fila. Al final de la fila, incrementa el puntero por el ancho del intervalo de la imagen, lo que hace avanzar el puntero a la fila siguiente.

En este ejemplo se llama a una función hipotética denominada TransformPixelValue para cada píxel. Podría ser cualquier función que calcule un píxel de destino a partir de un píxel de origen. Por supuesto, los detalles exactos dependerán de la tarea concreta. Por ejemplo, si tiene un formato YUV planar, debe tener acceso a los planos de zona independientemente del plano luma; con vídeo entrelazado, es posible que tenga que procesar los campos por separado. y así sucesivamente.

Para proporcionar un ejemplo más concreto, el código siguiente convierte una imagen RGB de 32 bits en una imagen de AYUV. Se accede a los píxeles RGB mediante una estructura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) y se accede a los píxeles AYUV mediante una estructura de estructura [**\_ DXVA2 AYUVSample8.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8)


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



En el ejemplo siguiente se convierte una imagen RGB de 32 bits en una imagen YV12. En este ejemplo se muestra cómo controlar un formato YUV planar. (YV12 es un formato planar 4:2:0). En este ejemplo, la función mantiene tres punteros independientes para los tres planos de la imagen de destino. Sin embargo, el enfoque básico es el mismo que el ejemplo anterior.


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



En todos estos ejemplos, se supone que la aplicación ya ha determinado el paso de la imagen. A veces puede obtener esta información del búfer multimedia. De lo contrario, debe calcularlo en función del formato de vídeo. Para obtener más información sobre cómo calcular el paso de la imagen y trabajar con búferes multimedia para vídeo, vea [Búferes de vídeo sin comprimir.](uncompressed-video-buffers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 
