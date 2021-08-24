---
description: Describe los formatos de archivo de imagen admitidos. Vea Comentarios para obtener descripciones de estos formatos.
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: D3DXIMAGE_FILEFORMAT enumeración (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_FILEFORMAT
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 715b9f0f6d8c56153d51c9c19b70ba253e508619229f52201a28f23c1902d26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123171"
---
# <a name="d3dximage_fileformat-enumeration"></a>D3DXIMAGE \_ FILEFORMAT (enumeración)

Describe los formatos de archivo de imagen admitidos. Vea Comentarios para obtener descripciones de estos formatos.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXIMAGE_FILEFORMAT { 
  D3DXIFF_BMP          = 0,
  D3DXIFF_JPG          = 1,
  D3DXIFF_TGA          = 2,
  D3DXIFF_PNG          = 3,
  D3DXIFF_DDS          = 4,
  D3DXIFF_PPM          = 5,
  D3DXIFF_DIB          = 6,
  D3DXIFF_HDR          = 7,
  D3DXIFF_PFM          = 8,
  D3DXIFF_FORCE_DWORD  = 0x7fffffff
} D3DXIMAGE_FILEFORMAT, *LPD3DXIMAGE_FILEFORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**
</dt> <dd>

Windows formato de archivo de mapa de bits (BMP).

</dd> <dt>

<span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ JPG**
</dt> <dd>

Formato de archivo comprimido del Grupo de expertos de la fotografía conjunta (JPEG).

</dd> <dt>

<span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF \_ TGA**
</dt> <dd>

Formato de archivo de imagen Truevision (Targa o TGA).

</dd> <dt>

<span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF \_ PNG**
</dt> <dd>

Formato de archivo portable de gráficos de red (PNG).

</dd> <dt>

<span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF \_ DDS**
</dt> <dd>

Formato de archivo de superficie de DirectDraw (DDS).

</dd> <dt>

<span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ PPM**
</dt> <dd>

Formato de archivo portablemap (PPM).

</dd> <dt>

<span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF \_ DIB**
</dt> <dd>

Windows archivo de mapa de bits independiente del dispositivo (DIB).

</dd> <dt>

<span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF \_ HDR**
</dt> <dd>

Formato de archivo de alto rango dinámico (HDR).

</dd> <dt>

<span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**
</dt> <dd>

Formato de archivo de mapa flotante portátil.

</dd> <dt>

<span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las funciones que comienzan por D3DXLoadxxx admiten todos los formatos enumerados. Las funciones que comienzan por D3DXSavexxx admiten todos los formatos enumerados, excepto los formatos Truevision (.tga) y portablemap (.ppm).

En la tabla siguiente se enumeran los formatos de entrada y salida disponibles.



| Extensión de archivo | Descripción                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .bmp           | Windows de mapa de bits. Contiene un encabezado que describe la resolución del dispositivo en el que se creó el rectángulo de píxeles, las dimensiones del rectángulo, el tamaño de la matriz de bits, una paleta lógica y una matriz de bits que define la relación entre los píxeles de la imagen de mapa de bits y las entradas de la paleta lógica. |
| .dds           | Formato de archivo de DirectDraw Surface. Almacena texturas, texturas de volumen y mapas de entornos cúbicas, con o sin niveles de mapa mipmap y con o sin compresión de píxeles. Vea [DDS.](../direct3ddds/dx-graphics-dds.md)                                                                                                                                       |
| .dib           | Windows Dib. Contiene una matriz de bits combinada con estructuras que especifican el ancho y alto de la imagen de mapa de bits, el formato de color del dispositivo donde se creó la imagen y la resolución del dispositivo usado para crear esa imagen.                                                                                                              |
| .hdr           | Formato HDR. Codifica cada píxel como un color RGBE de 32 bits, con 8 bits de mantisa para rojo, verde y azul, y un exponente compartido de 8 bits. Cada canal se comprime por separado con codificación de longitud de ejecución (RLE).                                                                                                                                       |
| .jpg           | Estándar JPEG. Especifica la compresión variable de los archivos de documento de color RGB de 24 bits y de escala Tagged Image File Format gris (TIFF) de 8 bits.                                                                                                                                                                                                       |
| .pfm           | Formato de mapa flotante portátil. Formato de imagen de punto flotante sin formato, sin compresión. El encabezado de archivo especifica el ancho de la imagen, el alto, el monocromo o el color, y el orden de las palabras de la máquina. Los datos de píxel se almacenan como valores de punto flotante de 32 bits, con 3 valores por píxel para color y un valor por píxel para monocromo.                                |
| .png           | Formato PNG. Formato de mapa de bits no propietario que usa la compresión sin pérdida.                                                                                                                                                                                                                                                                            |
| .ppm           | Formato portable deMap. Formato de archivo binario o ASCII para imágenes de color que incluye el alto y ancho de la imagen y el valor máximo del componente de color.                                                                                                                                                                                                 |
| .tga           | Formato targa o adaptador de gráficos de Truevision. Admite profundidades de 8, 15, 16, 24 y 32 bits, incluida la escala de grises de 8 bits, y contiene datos opcionales de la paleta de colores, datos de origen y tamaño de imagen (x, y) y datos de píxeles.                                                                                                                               |



 

Vea [Tipos de mapas de bits](../gdiplus/-gdiplus-types-of-bitmaps-about.md) para obtener más información sobre algunos de estos formatos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9tex.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
