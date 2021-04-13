---
description: Describe los formatos de archivo de imagen compatibles. Vea la sección Comentarios para obtener descripciones de estos formatos.
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: Enumeración D3DXIMAGE_FILEFORMAT (D3dx9tex. h)
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
ms.openlocfilehash: 3b1195e7503ff32e92cdbafde941b811dcf86427
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362565"
---
# <a name="d3dximage_fileformat-enumeration"></a>\_Enumeración de D3DXIMAGE FILEFORMAT

Describe los formatos de archivo de imagen compatibles. Vea la sección Comentarios para obtener descripciones de estos formatos.

## <a name="syntax"></a>Sintaxis


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

Formato de archivo de mapa de bits de Windows (BMP).

</dd> <dt>

<span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ jpg**
</dt> <dd>

Formato de archivo comprimido de JPEG (Joint Graphics Experts Group).

</dd> <dt>

<span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF \_ TGA**
</dt> <dd>

Formato de archivo de imagen Truevision (Targa o TGA).

</dd> <dt>

<span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**\_PNG D3DXIFF**
</dt> <dd>

Formato de archivo PNG (Portable Network Graphics).

</dd> <dt>

<span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF \_ DDS**
</dt> <dd>

Formato de archivo de DirectDraw Surface (DDS).

</dd> <dt>

<span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ ppm**
</dt> <dd>

Formato de archivo portable pixmap (PPM).

</dd> <dt>

<span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF \_ DIB**
</dt> <dd>

Formato de archivo de mapa de bits independiente del dispositivo (DIB) de Windows.

</dd> <dt>

<span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF \_ HDR**
</dt> <dd>

Formato de archivo de intervalo dinámico alto (HDR).

</dd> <dt>

<span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**\_PFM D3DXIFF**
</dt> <dd>

Formato de archivo de asignación Float portátil.

</dd> <dt>

<span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las funciones que comienzan por D3DXLoadxxx admiten todos los formatos enumerados. Las funciones que comienzan por D3DXSavexxx admiten todos los formatos enumerados, excepto los formatos Truevision (. TGA) y pixmap (. ppm) portable.

En la tabla siguiente se enumeran los formatos de entrada y salida disponibles.



| Extensión de archivo | Descripción                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .bmp           | Formato de mapa de bits de Windows. Contiene un encabezado que describe la resolución del dispositivo en el que se creó el rectángulo de píxeles, las dimensiones del rectángulo, el tamaño de la matriz de bits, una paleta lógica y una matriz de bits que define la relación entre los píxeles de la imagen de mapa de bits y las entradas de la paleta lógica. |
| .dds           | Formato de archivo de superficie de DirectDraw. Almacena texturas, texturas de volumen y mapas de entorno cúbicos, con o sin niveles de mipmap y con o sin compresión de píxeles. Consulte [DDS](../direct3ddds/dx-graphics-dds.md).                                                                                                                                       |
| .dib           | DIB de Windows. Contiene una matriz de bits combinados con estructuras que especifican el ancho y el alto de la imagen de mapa de bits, el formato de color del dispositivo en el que se creó la imagen y la resolución del dispositivo que se usa para crear la imagen.                                                                                                              |
| . HDR           | Formato HDR. Codifica cada píxel como un color de RGBE de 32 bits, con 8 bits de mantisa para rojo, verde y azul, y un exponente de 8 bits compartido. Cada canal se comprime por separado con la codificación de longitud de ejecución (RLE).                                                                                                                                       |
| .jpg           | Estándar JPEG. Especifica la compresión variable del color RGB de 24 bits y los archivos de documento de imagen de Tagged Image File Format de escala gris (TIFF) de 8 bits.                                                                                                                                                                                                       |
| . PFM           | Formato de mapa Float portátil. Formato de imagen de punto flotante sin formato, sin compresión. El encabezado de archivo especifica el ancho de la imagen, el alto, monocromo o color, y el orden de las palabras del equipo. Los datos de píxeles se almacenan como valores de punto flotante de 32 bits, con 3 valores por píxel para el color y un valor por píxel para monocromo.                                |
| .png           | Formato PNG. Formato de mapa de bits no propietario mediante compresión sin pérdida.                                                                                                                                                                                                                                                                            |
| . ppm           | Formato Pixmap portátil. Formato de archivo binario o ASCII para imágenes de color que incluye el alto y el ancho de la imagen y el valor del componente de color máximo.                                                                                                                                                                                                 |
| .tga           | Formato del adaptador de gráficos Targa o Truevision. Admite profundidades de 8, 15, 16, 24 y 32 bits, incluida la escala de grises de 8 bits, y contiene datos de paleta de colores opcionales, datos de origen y de tamaño de imagen (x, y) y datos de píxeles.                                                                                                                               |



 

Vea [tipos de mapas de bits](../gdiplus/-gdiplus-types-of-bitmaps-about.md) para obtener más información sobre algunos de estos formatos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9tex. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
