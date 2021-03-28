---
title: Enumeración D3DX11_IMAGE_FILE_FORMAT (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Formatos de archivo de imagen compatibles con las funciones D3DX11Createxxx y D3DX11Savexxx.
ms.assetid: 89fa9ab8-3be0-4dc5-a533-94edb01df36a
keywords:
- Enumeración de D3DX11_IMAGE_FILE_FORMAT Direct3D 11
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
ms.openlocfilehash: 730ce59bb8a07f3fd8ef78bbeb27b4d01d198f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987217"
---
# <a name="d3dx11_image_file_format-enumeration"></a>\_ \_ Enumeración de formato de archivo de imagen D3DX11 \_

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

Formatos de archivo de imagen compatibles con las funciones D3DX11Createxxx y D3DX11Savexxx.

## <a name="syntax"></a>Sintaxis


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

<span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ IFF, \_ BMP**
</dt> <dd>

Formato de archivo de mapa de bits de Windows (BMP). Contiene un encabezado que describe la resolución del dispositivo en el que se creó el rectángulo de píxeles, las dimensiones del rectángulo, el tamaño de la matriz de bits, una paleta lógica y una matriz de bits que define la relación entre los píxeles de la imagen de mapa de bits y las entradas de la paleta lógica. La extensión de archivo para este formato es. bmp.

</dd> <dt>

<span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11 \_ IFF \_ jpg**
</dt> <dd>

Formato de archivo comprimido JPEG (Joint Photographic Experts Group). Especifica la compresión variable del color RGB de 24 bits y los archivos de documento de imagen de Tagged Image File Format de escala gris (TIFF) de 8 bits. La extensión de archivo para este formato es. jpg.

</dd> <dt>

<span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**\_PNG D3DX11 IFF \_**
</dt> <dd>

Formato de archivo PNG (Portable Network Graphics). Formato de mapa de bits no propietario mediante compresión sin pérdida. La extensión de archivo para este formato es. png.

</dd> <dt>

<span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ IFF ( \_ DDS)**
</dt> <dd>

Formato de archivo de DirectDraw Surface (DDS). Almacena texturas, texturas de volumen y mapas de entorno cúbicos, con o sin niveles de mipmap y con o sin compresión de píxeles. La extensión de archivo para este formato es. DDS.

</dd> <dt>

<span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**\_TIFF IFF \_ D3DX11**
</dt> <dd>

Tagged Image File Format (TIFF). Las extensiones de archivo para este formato son. tif y. tiff.

</dd> <dt>

<span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**\_GIF IFF \_ D3DX11**
</dt> <dd>

Formato de intercambio de gráficos (GIF). La extensión de archivo para este formato es. gif.

</dd> <dt>

<span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11 \_ el \_ WMP IFF**
</dt> <dd>

Formato de Windows Media Photo (WMP). Este formato también se conoce como HD Photo y JPEG XR. Las extensiones de archivo para este formato son. HDP,. jxr y. WDP.

Para que funcione correctamente, D3DX11, a la vez, **\_ \_ WMP** le requiere que inicialice com. Por lo tanto, llame a [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) en la aplicación antes de llamar a D3DX.

</dd> <dt>

<span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ IFF \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Vea [tipos de mapas de bits (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) para obtener más información sobre algunos de estos formatos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

