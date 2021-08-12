---
title: Ejemplo de mapa de cubo de DDS
description: En el caso de los mapas de entorno cúbicas, una o varias caras de un cubo se escriben en el archivo, con formatos sin comprimir o comprimidos, y todas las caras deben tener el mismo tamaño.
ms.assetid: a77234f6-ba10-40dd-902f-33e600384aa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97a51526570a775eb0cff8ec5ed665ac3dc4b218a876743b29e983bd9c03e9ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289867"
---
# <a name="dds-cube-map-example"></a>Ejemplo de mapa de cubo de DDS

En el caso de los mapas de entorno cúbicas, una o varias caras de un cubo se escriben en el archivo, con formatos sin comprimir o comprimidos, y todas las caras deben tener el mismo tamaño. Cada cara puede tener mapas mip definidos, aunque todas las caras deben tener el mismo número de niveles de mapa mip. Si un archivo contiene un mapa de cubo, se deben establecer DDSCAPS COMPLEX, DDSCAPS2 CUBEMAP y uno o varios de \_ \_ DSCAPS2 \_ CUBEMAP \_ POSITIVEX/Y/Z o DDSCAPS2 \_ CUBEMAP \_ NEGATIVEX/Y/Z. Las caras se escriben en el orden: positivo x, x negativo, positivo y, negativo y, positivo z, z negativo, con las caras que faltan omitidas. Cada cara se escribe con su imagen principal, seguida de cualquier nivel de mapa mip.

Por ejemplo, un mapa de cubo de 256 por 256 con caras x positivas, negativas y z positivas, un formato de píxeles DXT1 y todos los niveles de mapa mip contendrán lo siguiente:



| Componentes de DDS                                      | \# Bytes |
|-----------------------------------------------------|----------|
| encabezado                                              | 128      |
| Imagen principal positiva de 256 por 256                    | 32 768    |
| Imagen mipmap positiva de 128 por 128                  | 8192     |
| Imagen mipmap positiva de 64 por 64                    | 2048     |
| Imagen mipmap positiva de 32 por 32                    | 512      |
| Imagen mipmap positiva de 16 por 16                    | 128      |
| Imagen mipmap positiva de 8 por 8                      | 32       |
| Imagen mipmap positiva de 4 por 4                      | 8        |
| Imagen mipmap positiva de 2 por 2                      | 8        |
| Imagen mipmap positiva de 1 por 1                      | 8        |
| repetir las 9 capas anteriores para la imagen mipmap y | 43704    |
| repetir las 9 capas anteriores para la imagen z mipmap | 43704    |



 

A partir de DirectX 8, un mapa de cubo se almacena con todas las caras definidas.

## <a name="dxgi-cube-maps"></a>Mapas de Mapas DXGI

Los mapas de entornos cúbicas de Direct3D 10.x y Direct3D 11 son equivalentes a una matriz de texturas 2D con 6 imágenes y se pueden almacenar en archivos DDS como tales. Con Direct3D 10.1 y Direct3D 11, el hardware también puede admitir matrices de mapas de cubo que son matrices de textura 2D con un múltiplo de 6 imágenes (6, 12, 18, 24, etc.).

Por ejemplo, este es un mapa de cubo de 256 por 256 con niveles de mapa mip almacenados en un formato BC6H como una matriz de texturas 2D:



| Componentes de DDS                                                                                                                                                                                                  | \# Bytes |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| header (FourCC de "DX10")                                                                                                                                                                                       | 128      |
| encabezado extendido (formato DXGI establecido en 95 \[ DXGI \_ FORMAT \_ BC6H UF16, valor de dimensión \_ de \] \[ 3 D3Dxx RESOURCE DIMENSION TEXTURE2D, tamaño de \_ \_ \_ \] matriz de 6, marcas misc de \[ 0x4 D3Dxx \_ RESOURCE \_ MISC \_ TEXTURECUBE \] ) | 20       |
| 256-by-256 array entry 0 (positive x) main image (256-by-256 array entry 0 (positive x) main image                                                                                                                                                                | 65536    |
| 128-by-128 array entry 0 (positive x) mipmap image                                                                                                                                                              | 16384    |
| Imagen mipmap de entrada de matriz 64 por 64 0 (x positivo)                                                                                                                                                                | 4096     |
| Imagen mipmap de entrada de matriz 0 (x positivo) de 32 por 32                                                                                                                                                                | 1024     |
| 16-by-16 array entry 0 (positive x) mipmap image (16-by-16 array entry 0 (positive x) mipmap image                                                                                                                                                                | 256      |
| Imagen mipmap de entrada de matriz 8 por 8 (x positivo)                                                                                                                                                                  | 64       |
| Imagen mipmap de entrada de matriz 4 por 4 (x positivo)                                                                                                                                                                  | 16       |
| Imagen mipmap de entrada de matriz 2 por 2 (x positiva)                                                                                                                                                                  | 16       |
| Imagen mipmap de entrada de matriz 1 por 1 (x positivo)                                                                                                                                                                  | 16       |
| repetir las 9 capas anteriores para la entrada de matriz 1 (x negativo) imagen mipmap                                                                                                                                        | 87408    |
| repetir las 9 capas anteriores para la entrada de matriz 2 (positivo y) imagen mipmap                                                                                                                                        | 87408    |
| repetir las 9 capas anteriores para la entrada de matriz 3 (y negativo) imagen de mapa mip                                                                                                                                        | 87408    |
| repetir las 9 capas anteriores para la entrada de matriz 4 (z positivo) imagen mipmap                                                                                                                                        | 87408    |
| repetir las 9 capas anteriores para la entrada de matriz 5 (z negativo) imagen mipmap                                                                                                                                        | 87408    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




