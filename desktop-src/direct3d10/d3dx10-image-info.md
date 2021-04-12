---
description: Devuelve una descripción del contenido original de un archivo de imagen.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: D3DX10_IMAGE_INFO estructura (D3DX10. h)
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
ms.openlocfilehash: bf240296610c083e0d042d187ae29054461193a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362487"
---
# <a name="d3dx10_image_info-structure"></a>Estructura de información de \_ imagen de D3DX10 \_

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de la imagen original en píxeles.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto de la imagen original en píxeles.

</dd> <dt>

**Profundidad**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Profundidad de la imagen original en píxeles.

</dd> <dt>

**ArraySize**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño de la matriz de textura. *Tamaño* será 1 para una sola imagen.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de niveles de mipmap en la imagen original.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Propiedades de recursos misceláneas (consulte la [**marca D3D10 de \_ recursos \_ varios \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[ **\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Un valor del tipo [**de \_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enumerado que describe mejor los datos de la imagen original.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Tipo: **[ **\_ \_ dimensión de recursos D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Representa el tipo de la textura almacenada en el archivo. Consulte [**\_ \_ dimensión de recursos D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: **[ **\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md)**

</dd> <dd>

Representa el formato del archivo de imagen. Consulte [**\_ formato de \_ archivo \_ de imagen D3DX10**](d3dx10-image-file-format.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
