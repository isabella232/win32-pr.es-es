---
description: Formatos de archivo de imagen compatibles con las funciones D3DXCreatexxx y D3DX10Savexxx.
ms.assetid: 39602f3c-5c91-4667-96d0-c3bdba712d88
title: D3DX10_IMAGE_FILE_FORMAT enumeración (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_FILE_FORMAT
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: fba878a40f510cc5e76256161255e01deaa7ee04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063803"
---
# <a name="d3dx10_image_file_format-enumeration"></a>Enumeración D3DX10 \_ IMAGE \_ FILE \_ FORMAT

Formatos de archivo de imagen compatibles con las funciones D3DXCreatexxx y D3DX10Savexxx.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DX10_IMAGE_FILE_FORMAT { 
  D3DX10_IFF_BMP          = 0,
  D3DX10_IFF_JPG          = 1,
  D3DX10_IFF_PNG          = 3,
  D3DX10_IFF_DDS          = 4,
  D3DX10_IFF_TIFF         = 10,
  D3DX10_IFF_GIF          = 11,
  D3DX10_IFF_WMP          = 12,
  D3DX10_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX10_IMAGE_FILE_FORMAT, *LPD3DX10_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ IFF \_ BMP**
</dt> <dd>

Windows formato de archivo de mapa de bits (BMP). Contiene un encabezado que describe la resolución del dispositivo en el que se creó el rectángulo de píxeles, las dimensiones del rectángulo, el tamaño de la matriz de bits, una paleta lógica y una matriz de bits que define la relación entre los píxeles de la imagen de mapa de bits y las entradas de la paleta lógica. La extensión de archivo para este formato es .bmp.

</dd> <dt>

<span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10 \_ IFF \_ JPG**
</dt> <dd>

Formato de archivo comprimido del Grupo de expertos de fotografía conjunta (JPEG). Especifica la compresión variable de los archivos de documento de imagen TIFF (color RGB de 24 bits) Tagged Image File Format escala de grises de 8 bits. La extensión de archivo para este formato es .jpg.

</dd> <dt>

<span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10 \_ IFF \_ PNG**
</dt> <dd>

Formato de archivo portable de gráficos de red (PNG). Formato de mapa de bits no propietario que usa compresión sin pérdida. La extensión de archivo para este formato es .png.

</dd> <dt>

<span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ IFF \_ DDS**
</dt> <dd>

Formato de archivo de superficie DirectDraw (DDS). Almacena texturas, texturas de volumen y mapas de entornos cúbicas, con o sin niveles de mapa mipmap, y con o sin compresión de píxeles. La extensión de archivo para este formato es .dds.

</dd> <dt>

<span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10 \_ IFF \_ TIFF**
</dt> <dd>

Tagged Image File Format (TIFF). Las extensiones de archivo para este formato son .tif y .tiff.

</dd> <dt>

<span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**GIF DE IFF D3DX10 \_ \_**
</dt> <dd>

Formato de intercambio de gráficos (GIF). La extensión de archivo para este formato es .gif.

</dd> <dt>

<span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10 \_ IFF \_ WMP**
</dt> <dd>

Windows Formato de foto multimedia (WMP). Este formato también se conoce como HD Photo y JPEG XR. Las extensiones de archivo para este formato son .hdp, .jxr y .wdp.

Para que funcione correctamente, **D3DX10 \_ IFF \_ WMP** requiere que inicialice COM. Por lo tanto, llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) [**o CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) en la aplicación antes de llamar a D3DX.

</dd> <dt>

<span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ IFF \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase a un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Consulte [Tipos de mapas de bits (GDI+) para](../gdiplus/-gdiplus-types-of-bitmaps-about.md) obtener más información sobre algunos de estos formatos.

D3DX10 usa el componente Windows imaging para implementar la mayoría de los tipos de archivo de mapa de bits admitidos. Consulte [información Windows de componentes de creación de imágenes](https://msdn.microsoft.com/library/ms737408.aspx) para obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
