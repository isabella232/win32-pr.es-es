---
title: Ejemplo de mapa de cubo DDS
description: En el caso de las asignaciones de entorno cúbicas, se escriben una o varias caras de un cubo en el archivo, con formatos comprimidos o sin comprimir, y todas las caras deben tener el mismo tamaño.
ms.assetid: a77234f6-ba10-40dd-902f-33e600384aa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235749bc0cf95a2e2120f66f3bcfb8a46e158628
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532242"
---
# <a name="dds-cube-map-example"></a>Ejemplo de mapa de cubo DDS

En el caso de las asignaciones de entorno cúbicas, se escriben una o varias caras de un cubo en el archivo, con formatos comprimidos o sin comprimir, y todas las caras deben tener el mismo tamaño. Cada cara puede tener mapas MIP definidos, aunque todas las caras deben tener el mismo número de niveles de mipmap. Si un archivo contiene un mapa de cubo, DDSCAPS \_ Complex, DDSCAPS2 \_ mapa, y se deben establecer uno o varios DSCAPS2 \_ mapa POSITIVEX \_ /y/z y/o DDSCAPS2 mapa NEGATIVEX \_ \_ /Y/z. Las caras se escriben en el orden: x positivo, x negativo, positivo y, negativo y, positivo z, negativo z, donde se omiten las caras que faltan. Cada una de las caras se escribe con la imagen principal, seguida de los niveles de mipmap.

Por ejemplo, un mapa de cubo de 256 por 256 con caras x, negativas y y números z positivos, un formato de píxel de DXT1 y todos los niveles de mipmap contendrían lo siguiente:



| Componentes DDS                                      | \# Bytes |
|-----------------------------------------------------|----------|
| header                                              | 128      |
| imagen principal x positiva 256-by-256                    | 32 768    |
| 128-por-128 positivo x imagen de mipmap                  | 8192     |
| 64-por-64 positivo x imagen de mipmap                    | 2048     |
| 32-por-32 positivo x imagen de mipmap                    | 512      |
| imagen de mipmap x de 16 por 16 positivo                    | 128      |
| imagen de mipmap x de 8 por 8 positivos                      | 32       |
| imagen de mapa de bits x positivo de 4 por 4                      | 8        |
| imagen de mapa de bits x positivo de 2 por 2                      | 8        |
| imagen de mipmap de 1 por 1 positivo x                      | 8        |
| repetir las 9 capas anteriores para la imagen de mipmap de y | 43704    |
| repetir las 9 capas anteriores para la imagen de MIP de z | 43704    |



 

A partir de DirectX 8, se almacena un mapa de cubo con todas las caras definidas.

## <a name="dxgi-cube-maps"></a>Mapas de cubos de DXGI

Los mapas de entorno cúbicos en Direct3D 10. x y Direct3D 11 son equivalentes a una matriz de textura 2D con seis imágenes y se pueden almacenar en archivos DDS como tal. Con Direct3D 10,1 y Direct3D 11, el hardware también puede admitir matrices de cubemaps, que son matrices de texturas bidimensionales con un múltiplo de 6 imágenes (6, 12, 18, 24, etc.).

Por ejemplo, a continuación se muestra un mapa de 256 por 256 con niveles de mipmap almacenados en un formato BC6H como una matriz de textura 2D:



| Componentes DDS                                                                                                                                                                                                  | \# Bytes |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| header (FourCC de "contenido DX10")                                                                                                                                                                                       | 128      |
| encabezado extendido (el formato de DXGI se establece en \[ \_ el formato 95 DXGI \_ BC6H \_ UF16 \] , el valor de dimensión 3 \[ D3Dxx \_ de la dimensión de recursos \_ \_ TEXTURE2D \] , el tamaño de la matriz de 6, las marcas Misc de 0x4 \[ D3Dxx de \_ recursos \_ varios \_ TEXTURECUBE \] ) | 20       |
| 256-por-256 matriz entrada 0 (x positivo) imagen principal                                                                                                                                                                | 65536    |
| 128 128: imagen de mipmap 0 (x positiva x) de la entrada de matriz                                                                                                                                                              | 16384    |
| 64 64: imagen de mipmap 0 (x positiva x) de la entrada de matriz                                                                                                                                                                | 4096     |
| 32 32: imagen de mipmap 0 (x positiva x) de la entrada de matriz                                                                                                                                                                | 1024     |
| imagen de mipmap 0 (x positiva x) de 16 por 16                                                                                                                                                                | 256      |
| entrada de la matriz de 8 por 8 (x positiva x) imagen de mipmap                                                                                                                                                                  | 64       |
| imagen de mipmap 0 (x positiva x) de 4 por 4 matriz                                                                                                                                                                  | 16       |
| imagen de mipmap 0 (x positiva x) de la entrada de matriz 2 por 2                                                                                                                                                                  | 16       |
| 1-por-1 entrada de matriz 0 (x positivo) imagen MIP                                                                                                                                                                  | 16       |
| repetir las 9 capas anteriores para la entrada de la matriz 1 (negativo x) imagen de mipmap                                                                                                                                        | 87408    |
| repetir las 9 capas anteriores para la entrada de la matriz 2 (y) imagen de mipmap                                                                                                                                        | 87408    |
| Repita los 9 niveles anteriores para la entrada de matriz 3 (y negativa) de la imagen de mipmap                                                                                                                                        | 87408    |
| repetir las 9 capas anteriores para la entrada de la matriz 4 (positiva z) imagen de mipmap                                                                                                                                        | 87408    |
| repetir las 9 capas anteriores para la entrada de la matriz 5 (z negativo) imagen de mipmap                                                                                                                                        | 87408    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




