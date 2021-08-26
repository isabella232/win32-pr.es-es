---
description: 'D3DX10_IMAGE_INFO estructura: devuelve una descripción del contenido original de un archivo de imagen.'
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: D3DX10_IMAGE_INFO estructura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: bf3aa2eeb3e908a76e05588940927fff53dd1583c937d95a1c862f6021bd630f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989525"
---
# <a name="d3dx10_image_info-structure"></a>Estructura DE INFORMACIÓN DE IMAGEN de D3DX10 \_ \_

Devuelve una descripción del contenido original de un archivo de imagen.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Width**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de la imagen original en píxeles.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto de la imagen original en píxeles.

</dd> <dt>

**Profundidad**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Profundidad de la imagen original en píxeles.

</dd> <dt>

**ArraySize**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño de la matriz de texturas. *ArraySize* será 1 para una sola imagen.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de niveles de mapa mip en la imagen original.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Propiedades de recursos varios (consulte [**D3D10 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[ **DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Valor del tipo [**enumerado DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que describe más de cerca los datos de la imagen original.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Tipo: **[ **DIMENSIÓN DE \_ RECURSOS \_ D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Representa el tipo de la textura almacenada en el archivo. Consulte [**DIMENSIÓN DE RECURSOS D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: FORMATO DE ARCHIVO DE **[ **\_ IMAGEN \_ \_ D3DX10**](d3dx10-image-file-format.md)**

</dd> <dd>

Representa el formato del archivo de imagen. Vea FORMATO DE ARCHIVO DE [**IMAGEN D3DX10 \_ \_ \_**](d3dx10-image-file-format.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
