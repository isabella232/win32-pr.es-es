---
description: 'D3DXIMAGE_INFO estructura: devuelve una descripción del contenido original de un archivo de imagen.'
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: D3DXIMAGE_INFO estructura (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: be70cc88645e0aac6734907c6a97f2d4bb104c99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359202"
---
# <a name="d3dximage_info-structure"></a>D3DXIMAGE \_ INFO (estructura)

Devuelve una descripción del contenido original de un archivo de imagen.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a>Members

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

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de niveles de mip en la imagen original.

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Valor del tipo [enumerado D3DFORMAT](d3dformat.md) que describe más de cerca los datos de la imagen original.

</dd> <dt>

**ResourceType**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Representa el tipo de la textura almacenada en el archivo. Es D3DRTYPE \_ TEXTURE, D3DRTYPE \_ VOLUMETEXTURE o D3DRTYPE \_ CubeTexture.

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

</dd> <dd>

Representa el formato del archivo de imagen.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9tex.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
