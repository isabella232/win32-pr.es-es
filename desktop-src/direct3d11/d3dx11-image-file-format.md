---
title: D3DX11_IMAGE_FILE_FORMAT enumeración (D3DX11tex.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store. Formatos de archivo de imagen admitidos por las funciones D3DX11Createxxx y D3DX11Savexxx.
ms.assetid: 89fa9ab8-3be0-4dc5-a533-94edb01df36a
keywords:
- D3DX11_IMAGE_FILE_FORMAT enumeración Direct3D 11
- LPD3DX11_IMAGE_FILE_FORMAT puntero de enumeración Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_FILE_FORMAT
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e34d3ab49987d499114c4b9eee695bfad02055fbbef785a955407e97843208f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536969"
---
# <a name="d3dx11_image_file_format-enumeration"></a>Enumeración D3DX11 \_ IMAGE \_ FILE \_ FORMAT

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Formatos de archivo de imagen admitidos por las funciones D3DX11Createxxx y D3DX11Savexxx.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_IMAGE_FILE_FORMAT { 
  D3DX11_IFF_BMP          = 0,
  D3DX11_IFF_JPG          = 1,
  D3DX11_IFF_PNG          = 3,
  D3DX11_IFF_DDS          = 4,
  D3DX11_IFF_TIFF         = 10,
  D3DX11_IFF_GIF          = 11,
  D3DX11_IFF_WMP          = 12,
  D3DX11_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX11_IMAGE_FILE_FORMAT, *LPD3DX11_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ IFF \_ BMP**
</dt> <dd>

Windows de archivo de mapa de bits (BMP). Contiene un encabezado que describe la resolución del dispositivo en el que se creó el rectángulo de píxeles, las dimensiones del rectángulo, el tamaño de la matriz de bits, una paleta lógica y una matriz de bits que define la relación entre los píxeles de la imagen de mapa de bits y las entradas de la paleta lógica. La extensión de archivo para este formato es .bmp.

</dd> <dt>

<span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11 \_ IFF \_ JPG**
</dt> <dd>

Formato de archivo comprimido del Grupo de expertos en fotografía conjunta (JPEG). Especifica la compresión variable de los archivos de documento de imagen de color RGB de 24 bits y de escala de Tagged Image File Format gris de 8 bits (TIFF). La extensión de archivo para este formato es .jpg.

</dd> <dt>

<span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11 \_ IFF \_ PNG**
</dt> <dd>

Formato de archivo portable de gráficos de red (PNG). Formato de mapa de bits no propietario que usa compresión sin pérdida. La extensión de archivo para este formato es .png.

</dd> <dt>

<span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ IFF \_ DDS**
</dt> <dd>

Formato de archivo de superficie de DirectDraw (DDS). Almacena texturas, texturas de volumen y mapas de entornos cúbicas, con o sin niveles de mapa mipmap y con o sin compresión de píxeles. La extensión de archivo para este formato es .dds.

</dd> <dt>

<span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11 \_ IFF \_ TIFF**
</dt> <dd>

Tagged Image File Format (TIFF). Las extensiones de archivo para este formato son .tif y .tiff.

</dd> <dt>

<span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**GIF DE IFF D3DX11 \_ \_**
</dt> <dd>

Formato de intercambio de gráficos (GIF). La extensión de archivo para este formato es .gif.

</dd> <dt>

<span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11 \_ IFF \_ WMP**
</dt> <dd>

Windows Formato de foto multimedia (WMP). Este formato también se conoce como HD Photo y JPEG XR. Las extensiones de archivo para este formato son .hdp, .jxr y .wdp.

Para que funcione correctamente, **D3DX11 \_ IFF \_ WMP** requiere que inicialice COM. Por lo tanto, llame a [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) [**o CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) en la aplicación antes de llamar a D3DX.

</dd> <dt>

<span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ IFF \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Consulte [Tipos de mapas de bits (GDI+) para](../gdiplus/-gdiplus-types-of-bitmaps-about.md) obtener más información sobre algunos de estos formatos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

