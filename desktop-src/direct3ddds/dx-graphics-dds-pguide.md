---
title: Guía de programación para DDS
description: Direct3D implementa el formato de archivo DDS para almacenar texturas sin comprimir o comprimidas (DXTn).
ms.assetid: 39f9847e-3b1c-4401-a253-74c183ffcc83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc1f8b9b84c2dc1f9236c79c320ae75848834ef2183db55b189f6b9d340d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796725"
---
# <a name="programming-guide-for-dds"></a>Guía de programación para DDS

Direct3D implementa el formato de archivo DDS para almacenar texturas sin comprimir o comprimidas (DXTn). El formato de archivo implementa varios tipos ligeramente diferentes diseñados para almacenar diferentes tipos de datos y admite texturas de una sola capa, texturas con mapas mip, mapas de cubos, mapas de volumen y matrices de texturas (en Direct3D 10/11). En esta sección se describe el diseño de un archivo DDS.

Para obtener ayuda para crear una textura en Direct3D 11, [vea Cómo: Crear una textura.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) Para obtener ayuda en Direct3D 9, vea Compatibilidad con [texturas en D3DX (Direct3D 9).](/windows/desktop/direct3d9/texture-support-in-d3dx)

-   [Diseño del archivo DDS](#dds-file-layout)
-   [Variantes de DDS](#dds-variants)
-   [Uso de matrices de textura en Direct3D 10/11](#using-texture-arrays-in-direct3d-1011)
-   [Formatos comunes de recursos de archivo DDS y contenido de encabezado asociado](#common-dds-file-resource-formats-and-associated-header-content)
-   [Temas relacionados](#related-topics)

## <a name="dds-file-layout"></a>Diseño del archivo DDS

Un archivo DDS es un archivo binario que contiene la siguiente información:

-   Un DWORD (número mágico) con el valor de código de cuatro caracteres 'DDS ' (0x20534444).

-   Una descripción de los datos del archivo.

    Los datos se describen con una descripción de encabezado mediante [**DDS \_ HEADER;**](dds-header.md)el formato de píxel se define mediante [**DDS \_ PIXELFORMAT**](dds-pixelformat.md). Tenga en cuenta que las estructuras **\_ DDS HEADER** y **DDS \_ PIXELFORMAT** reemplazan a las estructuras DDSURFACEDESC2, DDSCAPS2 y DDPIXELFORMAT DirectDraw 7 en desuso. **DDS \_ HEADER** es el equivalente binario de DDSURFACEDESC2 y DDSCAPS2. **DDS \_ PIXELFORMAT** es el equivalente binario de DDPIXELFORMAT.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
            
    ```

    

    Si DDS PIXELFORMAT dwFlags se establece en DDPF FOURCC y dwFourCC se establece en "DX10", habrá una estructura \_ \_ [**DDS \_ HEADER \_ DXT10**](dds-header-dxt10.md) adicional para dar cabida a matrices de textura o formatos DXGI que no se pueden expresar como formato de píxel RGB, como formatos de punto flotante, formatos sRGB, etc. Cuando la **estructura \_ \_ DXT10 de DDS HEADER** está presente, toda la descripción de los datos tendrá este aspecto.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
    DDS_HEADER_DXT10    header10;
    ```

    

-   Puntero a una matriz de bytes que contiene los datos de la superficie principal.
    ```
    BYTE bdata[]
    ```

    

-   Puntero a una matriz de bytes que contiene las superficies restantes, como los niveles de mapas MIP, caras de un mapa de cubos, profundidades de una textura de volumen. Sigue estos vínculos para obtener más información sobre el diseño de un archivo DDS para: una [textura](dds-file-layout-for-textures.md), un [mapa de cubos](dds-file-layout-for-cubic-environment-maps.md) o una [textura de volumen](dds-file-layout-for-volume-textures.md).

    ```
    BYTE bdata2[]
    ```

    

Para una amplia compatibilidad con hardware, se recomienda usar [**DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ R8G8B8A8 \_ SNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI FORMAT \_ \_ R16G16 \_ SNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ R8G8 \_ SNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ R8 \_ UNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ BC1 \_ UNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ BC1 \_ UNORM \_ SRGB,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ BC2 \_ UNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ BC2 \_ UNORM \_ SRGB,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI FORMAT \_ \_ BC3 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)o [**DXGI FORMAT \_ \_ BC3 \_ UNORM \_ SRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format.

Para obtener más información sobre los formatos de textura comprimida, vea Compresión de bloques de textura en [Direct3D 11](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11) y Compresión de [bloques (Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)

La biblioteca D3DX (por ejemplo, D3DX11.lib) y otras bibliotecas similares de forma no confiable o incoherente proporcionan el valor de inclinación en el miembro **dwPitchOrLinearSize** de la estructura [**\_ HEADER de DDS.**](dds-header.md) Por lo tanto, al leer y escribir en archivos DDS, se recomienda calcular el tono de una de las maneras siguientes para los formatos indicados:

-   Para los formatos comprimidos en bloque, calcule el tono como:

    max( 1, ((width+3)/4) ) \* block-size

    El tamaño del bloque es de 8 bytes para los formatos DXT1, BC1 y BC4, y de 16 bytes para otros formatos comprimidos en bloques.

-   Para los formatos R8G8 \_ B8G8, G8R8 G8B8, empaquetados UYVY heredados y empaquetados en YUY2 heredados, calcule el tono \_ como:

    ((width+1) >> 1) \* 4

-   Para otros formatos, calcule el tono como:

    ( bits \* de ancho por píxel + 7 ) / 8

    Se divide entre 8 para la alineación de bytes.

> [!Note]  
> El valor de inclinación que calcula no siempre es igual al que proporciona el tiempo de ejecución, que está alineado con DWORD en algunas situaciones y alineado en bytes en otras situaciones. Por lo tanto, se recomienda copiar una línea de examen a la vez en lugar de intentar copiar toda la imagen en una sola copia.

 

## <a name="dds-variants"></a>Variantes de DDS

Hay muchas herramientas que crean y consumen archivos DDS, pero pueden variar en los detalles de lo que requieren en el encabezado. Los escritores deben rellenar los encabezados lo máximo posible y los lectores deben comprobar los valores mínimos para obtener la máxima compatibilidad. Para validar un archivo DDS, un lector debe asegurarse de que el archivo tiene al menos 128 bytes para alojar el valor mágico y el encabezado básico, el valor mágico es 0x20534444 ("DDS"), el tamaño del encabezado DDS es 124 y el PIXELFORMAT de DDS en el tamaño del encabezado \_ \_ es 32. Si DDS PIXELFORMAT dwFlags se establece en DDPF FOURCC y dwFourCC se establece en "DX10", el tamaño total del archivo debe ser de al menos \_ \_ 148 bytes.

Hay algunas variantes comunes en uso en las que el formato de píxel se establece en un código FOURCC de DDPF donde dwFourCC se establece en un valor de enumeración \_ D3DFORMAT o DXGI \_ FORMAT. No hay ninguna manera de saber si un valor de enumeración es D3DFORMAT o DXGI FORMAT, por lo que se recomienda encarecidamente que la extensión "DX10" y el encabezado \_ DDS HEADER DXT10 se usen en su lugar para almacenar dxgiFormat cuando el PIXELFORMAT de DDS básico no pueda expresar \_ \_ el \_ formato.

Se debe preferir el formato PIXELFORMAT DDS estándar para obtener la máxima compatibilidad para almacenar datos RGB sin comprimir y datos DXT1-5, ya que no todas las herramientas de DDS admiten la extensión \_ DX10.

## <a name="using-texture-arrays-in-direct3d-1011"></a>Uso de matrices de textura en Direct3D 10/11

Las nuevas estructuras DDS [**(DDS \_ HEADER**](dds-header.md) y [**DDS \_ HEADER \_ DXT10)**](dds-header-dxt10.md)en Direct3D 10/11 amplían el formato de archivo DDS para admitir una matriz de texturas, que es un nuevo tipo de recurso en Direct3D 10/11. Este es un código de ejemplo que muestra cómo acceder a los distintos niveles de mapa mip en una matriz de texturas, mediante los nuevos encabezados.


```
DWORD               dwMagic;
DDS_HEADER          header;
DDS_HEADER_DXT10    header10;
   
for (int iArrayElement = 0; iArrayElement < header10.arraySize; iArrayElement++)
{
   for (int iMipLevel = 0; iMipLevel < header.dwMipMapCount; iMipLevel++)
   {
     ...
   }
}       
```



## <a name="common-dds-file-resource-formats-and-associated-header-content"></a>Formatos comunes de recursos de archivo DDS y contenido de encabezado asociado



| Formato de recurso                                                                            | dwFlags        | dwRGBBitCount | dwRBitMask | dwGBitMask | dwBBitMask | dwABitMask |
|--------------------------------------------------------------------------------------------|----------------|---------------|------------|------------|------------|------------|
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM<br/> D3DFMT \_ A8B8G8R8<br/>                       | DDS \_ RGBA      | 32            | 0xff       | 0xff00     | 0xff0000   | 0xff000000 |
| DXGI \_ FORMAT \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | DDS \_ RGBA      | 32            | 0xffff     | 0xffff0000 |            |            |
| \*\*<br/> DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM<br/> D3DFMT \_ A2B10G10R10<br/> | DDS \_ RGBA      | 32            | 0x3ff      | 0xffc00    | 0x3ff00000 |            |
| DXGI \_ FORMAT \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | DDS \_ RGB       | 32            | 0xffff     | 0xffff0000 |            |            |
| DXGI \_ FORMAT \_ B5G5R5A1 \_ UNORM<br/> D3DFMT \_ A1R5G5B5<br/>                       | DDS \_ RGBA      | 16            | 0x7c00     | 0x3e0      | 0x1f       | 0x8000     |
| DXGI \_ FORMAT \_ B5G6R5 \_ UNORM<br/> D3FMT \_ R5G6B5<br/>                            | DDS \_ RGB       | 16            | 0xf800     | 0x7e0      | 0x1f       |            |
| DXGI \_ A8 \_ UNORM<br/> D3DFMT \_ A8<br/>                                           | DDS \_ ALPHA     | 8             |            |            |            | 0xff       |
| D3DFMT \_ A8R8G8B8<br/>                                                                | DDS \_ RGBA      | 32            | 0xff0000   | 0xff00     | 0xff       | 0xff000000 |
| D3DFMT \_ X8R8G8B8<br/>                                                                | DDS \_ RGB       | 32            | 0xff0000   | 0xff00     | 0xff       |            |
| D3DFMT \_ X8B8G8R8<br/>                                                                | DDS \_ RGB       | 32            | 0xff       | 0xff00     | 0xff0000   |            |
| \*\*<br/> D3DFMT \_ A2R10G10B10<br/>                                             | DDS \_ RGBA      | 32            | 0x3ff00000 | 0xffc00    | 0x3ff      | 0xc0000000 |
| D3DFMT \_ R8G8B8<br/>                                                                  | DDS \_ RGB       | 24            | 0xff0000   | 0xff00     | 0xff       |            |
| D3DFMT \_ X1R5G5B5<br/>                                                                | DDS \_ RGB       | 16            | 0x7c00     | 0x3e0      | 0x1f       |            |
| D3DFMT \_ A4R4G4B4<br/>                                                                | DDS \_ RGBA      | 16            | 0xf00      | 0xf0       | 0xf        | 0xf000     |
| D3DFMT \_ X4R4G4B4<br/>                                                                | DDS \_ RGB       | 16            | 0xf00      | 0xf0       | 0xf        |            |
| D3DFMT \_ A8R3G3B2<br/>                                                                | DDS \_ RGBA      | 16            | 0xe0       | 0x1c       | 0x3        | 0xff00     |
| D3DFMT \_ A8L8<br/>                                                                    | DDS \_ LUMINANCE | 16            | 0xff       |            |            | 0xff00     |
| D3DFMT \_ L16<br/>                                                                     | DDS \_ LUMINANCE | 16            | 0xffff     |            |            |            |
| D3DFMT \_ L8<br/>                                                                      | DDS \_ LUMINANCE | 8             | 0xff       |            |            |            |
| D3DFMT \_ A4L4<br/>                                                                    | DDS \_ LUMINANCE | 8             | 0xf        |            |            | 0xf0       |



 



| Formato de recurso                                                                             | dwFlags     | dwFourCC |
|---------------------------------------------------------------------------------------------|-------------|----------|
| DXGI \_ FORMAT \_ BC1 \_ UNORM<br/> D3DFMT \_ DXT1<br/>                                 | DDS \_ FOURCC | "DXT1"   |
| DXGI \_ FORMAT \_ BC2 \_ UNORM<br/> D3DFMT \_ DXT3<br/>                                 | DDS \_ FOURCC | "DXT3"   |
| DXGI \_ FORMAT \_ BC3 \_ UNORM<br/> D3DFMT \_ DXT5<br/>                                 | DDS \_ FOURCC | "DXT5"   |
| \*<br/> DXGI \_ FORMAT \_ BC4 \_ UNORM<br/>                                           | DDS \_ FOURCC | "BC4U"   |
| \*<br/> DXGI \_ FORMAT \_ BC4 \_ SNORM<br/>                                           | DDS \_ FOURCC | "BC4S"   |
| \*<br/> DXGI \_ FORMAT \_ BC5 \_ UNORM<br/>                                           | DDS \_ FOURCC | "ATI2"   |
| \*<br/> DXGI \_ FORMAT \_ BC5 \_ SNORM<br/>                                           | DDS \_ FOURCC | "BC5S"   |
| DXGI \_ FORMAT \_ R8G8 \_ B8G8 \_ UNORM<br/> D3DFMT \_ R8G8 \_ B8G8<br/>                    | DDS \_ FOURCC | "RGBG"   |
| DXGI \_ FORMAT \_ G8R8 \_ G8B8 \_ UNORM<br/> D3DFMT \_ G8R8 \_ G8B8<br/>                    | DDS \_ FOURCC | "GRGB"   |
| \*<br/> DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM<br/> D3DFMT \_ A16B16G16R16<br/>  | DDS \_ FOURCC | 36       |
| \*<br/> DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM<br/> D3DFMT \_ Q16W16V16U16<br/>  | DDS \_ FOURCC | 110      |
| \*<br/> DXGI \_ FORMAT \_ R16 \_ FLOAT<br/> D3DFMT \_ R16F<br/>                   | DDS \_ FOURCC | 111      |
| \*<br/> DXGI \_ FORMAT \_ R16G16 \_ FLOAT<br/> D3DFMT \_ G16R16F<br/>             | DDS \_ FOURCC | 112      |
| \*<br/> DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT<br/> D3DFMT \_ A16B16G16R16F<br/> | DDS \_ FOURCC | 113      |
| \*<br/> DXGI \_ FORMAT \_ R32 \_ FLOAT<br/> D3DFMT \_ R32F<br/>                   | DDS \_ FOURCC | 114      |
| \*<br/> DXGI \_ FORMAT \_ R32G32 \_ FLOAT<br/> D3DFMT \_ G32R32F<br/>             | DDS \_ FOURCC | 115      |
| \*<br/> DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT<br/> D3DFMT \_ A32B32G32R32F<br/> | DDS \_ FOURCC | 116      |
| D3DFMT \_ DXT2<br/>                                                                     | DDS \_ FOURCC | "DXT2"   |
| D3DFMT \_ DXT4<br/>                                                                     | DDS \_ FOURCC | "DXT4"   |
| D3DFMT \_ UYVY<br/>                                                                     | DDS \_ FOURCC | "UYVY"   |
| D3DFMT \_ YUY2<br/>                                                                     | DDS \_ FOURCC | "YUY2"   |
| D3DFMT \_ CxV8U8<br/>                                                                   | DDS \_ FOURCC | 117      |
| Cualquier formato DXGI                                                                             | DDS \_ FOURCC | "DX10"   |



 

\* = Un lector DDS sólido debe ser capaz de controlar estos códigos de formato heredados. Sin embargo, este lector de DDS debe preferir usar la extensión de encabezado "DX10" cuando escribe estos códigos de formato para evitar ambigüedades.

\*\* = Debido a algunos problemas de larga duración en implementaciones comunes de lectores y escritores de DDS, la manera más sólida de escribir datos de tipo 10:10:10:2 es usar la extensión de encabezado "DX10" con el código [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) "24" (es decir, el valor DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM). Los datos D3DFMT \_ A2R10G10B10 deben convertirse en datos de tipo 10:10:10:2 antes de escribirse como un archivo DDS con formato \_ DXGI FORMAT \_ R10G10B10A2 \_ UNORM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dds](dx-graphics-dds.md)
</dt> </dl>

 

