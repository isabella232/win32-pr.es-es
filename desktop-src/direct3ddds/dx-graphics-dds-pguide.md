---
title: Guía de programación para DDS
description: Direct3D implementa el formato de archivo DDS para almacenar texturas sin comprimir o comprimidas (DXTn).
ms.assetid: 39f9847e-3b1c-4401-a253-74c183ffcc83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4940db5ec40e6ec0b907aa4ee7ce725cd585e961
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421627"
---
# <a name="programming-guide-for-dds"></a>Guía de programación para DDS

Direct3D implementa el formato de archivo DDS para almacenar texturas sin comprimir o comprimidas (DXTn). El formato de archivo implementa varios tipos ligeramente diferentes diseñados para almacenar diferentes tipos de datos y admite texturas de una capa, texturas con mapas de cubos, mapas de cubos, mapas de volumen y matrices de texturas (en Direct3D 10/11). En esta sección se describe el diseño de un archivo DDS.

Para obtener ayuda sobre cómo crear una textura en Direct3D 11, vea [Cómo: crear una textura](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create). Para obtener ayuda en Direct3D 9, consulte [compatibilidad con texturas en D3DX (Direct3D 9)](/windows/desktop/direct3d9/texture-support-in-d3dx).

-   [Diseño del archivo DDS](#dds-file-layout)
-   [Variantes de DDS](#dds-variants)
-   [Usar matrices de textura en Direct3D 10/11](#using-texture-arrays-in-direct3d-1011)
-   [Formatos de recursos de archivos DDS comunes y contenido de encabezado asociado](#common-dds-file-resource-formats-and-associated-header-content)
-   [Temas relacionados](#related-topics)

## <a name="dds-file-layout"></a>Diseño del archivo DDS

Un archivo DDS es un archivo binario que contiene la siguiente información:

-   Un DWORD (número mágico) con el valor de código de cuatro caracteres 'DDS ' (0x20534444).

-   Una descripción de los datos del archivo.

    Los datos se describen con una descripción de encabezado mediante el [**\_ encabezado DDS**](dds-header.md); el formato de píxel se define mediante los píxeles de [**DDS \_**](dds-pixelformat.md). Tenga en cuenta que el **\_ encabezado DDS** y las estructuras de **\_ PIXELFORMAT de DDS** reemplazan las estructuras DDSURFACEDESC2, DDSCAPS2 y DDPIXELFORMAT de DirectDraw 7 desusadas. **DDS \_ HEADER** es el equivalente binario de DDSURFACEDESC2 y DDSCAPS2. **DDS \_ PIXELFORMAT** es el equivalente binario de DDPIXELFORMAT.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
            
    ```

    

    Si la DDS \_ PIXELFORMAT dwFlags está establecida en DDPF \_ FourCC y dwFourCC se establece en "contenido DX10", se presentará una estructura de [**encabezado DDS adicional \_ \_ DXT10**](dds-header-dxt10.md) para acomodar las matrices de textura o los formatos de DXGI que no se pueden expresar como un formato de píxel RGB, como los formatos de punto flotante, los formatos sRGB, etc. Cuando la **estructura \_ \_ DXT10 del encabezado DDS** esté presente, toda la descripción de los datos tendrá el siguiente aspecto.

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

    

Para una amplia compatibilidad de hardware, se recomienda usar el [**formato de dxgi \_ \_ R8G8B8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), el [**formato de dxgi \_ \_ R8G8B8A8 \_ UNORM \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), el [**formato de dxgi \_ \_ R8G8B8A8 \_ SNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), el [**formato de dxgi \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), el [**formato de dxgi \_ \_ R16G16 \_ SNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), el formato de dxgi R8G8 SNORM, el formato de dxgi de la [**UNORM, el \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)formato de dxgi BC1 UNORM, el formato [**de dxgi \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ BC1 \_ UNORM \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), o el formato [**de dxgi BC2 \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_ UNORM \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) . [**\_ \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Para obtener más información sobre los formatos de textura comprimidos, vea [compresión de bloques de textura en Direct3D 11](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11) y [compresión de bloques (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression).

La biblioteca de D3DX (por ejemplo, D3DX11. lib) y otras bibliotecas similares no confiables o incoherentes proporcionan el valor de paso en el miembro **dwPitchOrLinearSize** de la estructura del [**\_ encabezado DDS**](dds-header.md) . Por lo tanto, cuando se leen y escriben en archivos DDS, se recomienda calcular el paso de una de las siguientes maneras para los formatos indicados:

-   En el caso de los formatos comprimidos en bloques, calcule el paso como:

    Max (1, ((ancho + 3)/4)) \* tamaño de bloque

    El tamaño del bloque es de 8 bytes para los formatos DXT1, BC1 y las texturas BC4, y 16 bytes para otros formatos comprimidos en bloques.

-   En el caso de \_ los formatos R8G8 B8G8, G8R8 \_ G8B8, Legacy UYVY-empaquetado y Legacy YUY2-envase, calcule el paso como:

    ((ancho + 1)  >> 1) \* 4

-   Para otros formatos, calcule el paso como:

    ( \* bits de ancho por píxel + 7)/8

    Divide por 8 para la alineación de bytes.

> [!Note]  
> El valor de paso que calcula no siempre es igual que el tiempo que proporciona el Runtime, que está alineado con DWORD en algunas situaciones y con alineación de bytes en otras situaciones. Por lo tanto, se recomienda copiar una línea de exploración a la vez en lugar de intentar copiar toda la imagen en una copia.

 

## <a name="dds-variants"></a>Variantes de DDS

Hay muchas herramientas que crean y consumen archivos DDS, pero pueden variar en los detalles de lo que requieren en el encabezado. Los escritores deben rellenar los encabezados como sea posible y los lectores deben comprobar los valores mínimos para obtener la máxima compatibilidad. Para validar un archivo DDS, un lector debe asegurarse de que el archivo tiene al menos 128 bytes de longitud para acomodar el valor mágico y el encabezado básico, que el valor mágico es 0x20534444 ("DDS"), el \_ tamaño del encabezado DDS es 124 y el tamaño de los valores de la parte \_ de encabezado dds es 32. Si la DDS \_ PIXELFORMAT dwFlags está establecida en DDPF \_ FourCC y dwFourCC se establece en "contenido DX10", el tamaño total del archivo debe ser de al menos 148 bytes.

Hay algunas variantes comunes en uso en las que el formato de píxel se establece en un \_ código FourCC de DDPF donde dwFourCC se establece en un \_ valor de enumeración de formato D3DFORMAT o DXGI. No hay ninguna manera de saber si un valor de enumeración es un D3DFORMAT o un formato de DXGI \_ , por lo que se recomienda encarecidamente que se use la extensión "contenido DX10" y el \_ encabezado de DXT10 del encabezado DDS \_ en su lugar para almacenar el dxgiFormat cuando los formatos de la DDS básicos \_ no pueden expresar el formato.

\_Se debe preferir la compatibilidad estándar de los valores de tipo PIXELFORMAT para la compatibilidad máxima con el almacenamiento de datos RGB sin comprimir y datos de DXT1-5, ya que no todas las herramientas DDS admiten la extensión contenido DX10.

## <a name="using-texture-arrays-in-direct3d-1011"></a>Usar matrices de textura en Direct3D 10/11

Las nuevas estructuras DDS ([**\_ encabezado DDS**](dds-header.md) y [**\_ encabezado dds \_ DXT10**](dds-header-dxt10.md)) en Direct3D 10/11 amplían el formato de archivo DDS para admitir una matriz de texturas, que es un nuevo tipo de recurso en Direct3D 10/11. Este es un código de ejemplo que muestra cómo obtener acceso a los diferentes niveles de mipmap en una matriz de texturas, con los nuevos encabezados.


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



## <a name="common-dds-file-resource-formats-and-associated-header-content"></a>Formatos de recursos de archivos DDS comunes y contenido de encabezado asociado



| Formato de recursos                                                                            | dwFlags        | dwRGBBitCount | dwRBitMask | dwGBitMask | dwBBitMask | dwABitMask |
|--------------------------------------------------------------------------------------------|----------------|---------------|------------|------------|------------|------------|
| Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM<br/> D3DFMT \_ A8B8G8R8<br/>                       | el \_ RGBA de DDS      | 32            | 0xFF       | 0xff00     | 0xff0000   | 0xff000000 |
| Formato de DXGI \_ \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | el \_ RGBA de DDS      | 32            | 0xFFFF     | 0xffff0000 |            |            |
| \*\*<br/> Formato de DXGI \_ \_ R10G10B10A2 \_ UNORM<br/> D3DFMT \_ A2B10G10R10<br/> | el \_ RGBA de DDS      | 32            | 0x3ff      | 0xffc00    | 0x3ff00000 |            |
| Formato de DXGI \_ \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | \_RGB DDS       | 32            | 0xFFFF     | 0xffff0000 |            |            |
| Formato de DXGI \_ \_ B5G5R5A1 \_ UNORM<br/> D3DFMT \_ A1R5G5B5<br/>                       | el \_ RGBA de DDS      | 16            | 0x7c00     | 0x3e0      | 0x1F       | 0x8000     |
| Formato de DXGI \_ \_ B5G6R5 \_ UNORM<br/> D3FMT \_ R5G6B5<br/>                            | \_RGB DDS       | 16            | 0xf800     | 0x7e0      | 0x1F       |            |
| UNORM de DXGI \_ a8 \_<br/> D3DFMT \_ A8<br/>                                           | alfa (DDS) \_     | 8             |            |            |            | 0xFF       |
| D3DFMT \_ A8R8G8B8<br/>                                                                | el \_ RGBA de DDS      | 32            | 0xff0000   | 0xff00     | 0xFF       | 0xff000000 |
| D3DFMT \_ X8R8G8B8<br/>                                                                | \_RGB DDS       | 32            | 0xff0000   | 0xff00     | 0xFF       |            |
| D3DFMT \_ X8B8G8R8<br/>                                                                | \_RGB DDS       | 32            | 0xFF       | 0xff00     | 0xff0000   |            |
| \*\*<br/> D3DFMT \_ A2R10G10B10<br/>                                             | el \_ RGBA de DDS      | 32            | 0x3ff00000 | 0xffc00    | 0x3ff      | 0xc0000000 |
| D3DFMT \_ R8G8B8<br/>                                                                  | \_RGB DDS       | 24            | 0xff0000   | 0xff00     | 0xFF       |            |
| D3DFMT \_ X1R5G5B5<br/>                                                                | \_RGB DDS       | 16            | 0x7c00     | 0x3e0      | 0x1F       |            |
| D3DFMT \_ A4R4G4B4<br/>                                                                | el \_ RGBA de DDS      | 16            | 0xf00      | 0xf0       | 0xF        | 0xf000     |
| D3DFMT \_ X4R4G4B4<br/>                                                                | \_RGB DDS       | 16            | 0xf00      | 0xf0       | 0xF        |            |
| D3DFMT \_ A8R3G3B2<br/>                                                                | el \_ RGBA de DDS      | 16            | 0xE0       | 0x1c       | 0x3        | 0xff00     |
| D3DFMT \_ A8L8<br/>                                                                    | \_luminancia DDS | 16            | 0xFF       |            |            | 0xff00     |
| D3DFMT \_ L16<br/>                                                                     | \_luminancia DDS | 16            | 0xFFFF     |            |            |            |
| D3DFMT \_ L8<br/>                                                                      | \_luminancia DDS | 8             | 0xFF       |            |            |            |
| D3DFMT \_ A4L4<br/>                                                                    | \_luminancia DDS | 8             | 0xF        |            |            | 0xf0       |



 



| Formato de recursos                                                                             | dwFlags     | dwFourCC |
|---------------------------------------------------------------------------------------------|-------------|----------|
| Formato de DXGI \_ \_ BC1 \_ UNORM<br/> D3DFMT \_ DXT1<br/>                                 | FourCC de DDS \_ | DXT1   |
| Formato de DXGI \_ \_ BC2 \_ UNORM<br/> D3DFMT \_ DXT3<br/>                                 | FourCC de DDS \_ | "DXT3"   |
| Formato de DXGI \_ \_ BC3 \_ UNORM<br/> D3DFMT \_ DXT5<br/>                                 | FourCC de DDS \_ | DXT5   |
| \*<br/> Formato de DXGI \_ \_ las texturas BC4 \_ UNORM<br/>                                           | FourCC de DDS \_ | "BC4U"   |
| \*<br/> Formato de DXGI \_ \_ las texturas BC4 \_ SNORM<br/>                                           | FourCC de DDS \_ | "BC4S"   |
| \*<br/> Formato de DXGI \_ \_ BC5 \_ UNORM<br/>                                           | FourCC de DDS \_ | "ATI2"   |
| \*<br/> Formato de DXGI \_ \_ BC5 \_ SNORM<br/>                                           | FourCC de DDS \_ | "BC5S"   |
| Formato de DXGI \_ \_ R8G8 \_ B8G8 \_ UNORM<br/> D3DFMT \_ R8G8 \_ B8G8<br/>                    | FourCC de DDS \_ | "RGBG"   |
| Formato de DXGI \_ \_ G8R8 \_ G8B8 \_ UNORM<br/> D3DFMT \_ G8R8 \_ G8B8<br/>                    | FourCC de DDS \_ | "GRGB"   |
| \*<br/> Formato de DXGI \_ \_ R16G16B16A16 \_ UNORM<br/> D3DFMT \_ A16B16G16R16<br/>  | FourCC de DDS \_ | 36       |
| \*<br/> Formato de DXGI \_ \_ R16G16B16A16 \_ SNORM<br/> D3DFMT \_ Q16W16V16U16<br/>  | FourCC de DDS \_ | 110      |
| \*<br/> Formato de DXGI \_ \_ R16 \_ float<br/> D3DFMT \_ R16F<br/>                   | FourCC de DDS \_ | 111      |
| \*<br/> Formato de DXGI \_ \_ R16G16 \_ float<br/> D3DFMT \_ G16R16F<br/>             | FourCC de DDS \_ | 112      |
| \*<br/> Formato de DXGI \_ \_ R16G16B16A16 \_ float<br/> D3DFMT \_ A16B16G16R16F<br/> | FourCC de DDS \_ | 113      |
| \*<br/> Formato de DXGI \_ \_ R32 \_ float<br/> D3DFMT \_ R32F<br/>                   | FourCC de DDS \_ | 114      |
| \*<br/> Formato de DXGI \_ \_ R32G32 \_ float<br/> D3DFMT \_ G32R32F<br/>             | FourCC de DDS \_ | 115      |
| \*<br/> Formato de DXGI \_ \_ R32G32B32A32 \_ float<br/> D3DFMT \_ A32B32G32R32F<br/> | FourCC de DDS \_ | 116      |
| D3DFMT \_ DXT2<br/>                                                                     | FourCC de DDS \_ | "DXT2"   |
| D3DFMT \_ DXT4<br/>                                                                     | FourCC de DDS \_ | "DXT4"   |
| D3DFMT \_ UYVY<br/>                                                                     | FourCC de DDS \_ | UYVY   |
| D3DFMT \_ YUY2<br/>                                                                     | FourCC de DDS \_ | YUY2   |
| D3DFMT \_ CxV8U8<br/>                                                                   | FourCC de DDS \_ | 117      |
| Cualquier formato de DXGI                                                                             | FourCC de DDS \_ | CONTENIDO DX10   |



 

\* = Un lector DDS robusto debe ser capaz de administrar estos códigos de formato heredados. Sin embargo, este lector DDS debe preferir utilizar la extensión de encabezado "contenido DX10" cuando escribe estos códigos de formato para evitar la ambigüedad.

\*\* = Debido a algunos problemas de larga duración en implementaciones comunes de lectores y escritores de DDS, la forma más sólida de escribir datos de tipo 10:10:10:2 es usar la extensión de encabezado "contenido DX10" con el código de [**\_ formato de dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) "24" (es decir, el formato de dxgi \_ \_ R10G10B10A2 \_ UNORM Value). Los \_ datos de D3DFMT A2R10G10B10 se deben convertir en datos de tipo 10:10:10:2 antes de escribirse como un archivo de formato de DXGI \_ \_ R10G10B10A2 \_ UNORM Format DDS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DDS](dx-graphics-dds.md)
</dt> </dl>

 

