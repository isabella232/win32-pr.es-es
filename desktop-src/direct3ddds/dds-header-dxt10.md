---
title: Estructura de DDS_HEADER_DXT10 (DDS. h)
description: Extensión de encabezado DDS para administrar matrices de recursos, formatos de píxeles de DXGI que no se asignan a las estructuras de formato de píxel de Microsoft DirectDraw heredadas y metadatos adicionales.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- Estructura de DDS_HEADER_DXT10 DDS
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a2f5dd4a6948d38b86b49584db81937ce5148b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717625"
---
# <a name="dds_header_dxt10-structure"></a>\_Estructura DXT10 del encabezado DDS \_

Extensión de encabezado DDS para administrar matrices de recursos, formatos de píxeles de DXGI que no se asignan a las estructuras de formato de píxel de Microsoft DirectDraw heredadas y metadatos adicionales.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dxgiFormat**
</dt> <dd>

Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

El formato de píxel de la superficie (consulte [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

</dd> <dt>

**resourceDimension**
</dt> <dd>

Tipo: **[ **\_ \_ dimensión de recursos D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Identifica el tipo de recurso. Los valores siguientes para este miembro son un subconjunto de los valores de [**la \_ \_ dimensión de recursos D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) o la enumeración de [**\_ \_ dimensiones de recursos D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) :



| Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                            | Value |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| \_TEXTURE1D de dimensión DDS \_ ( \_ dimensión de recursos D3D10 \_ \_ TEXTURE1D) | El recurso es una [textura 1D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types). El miembro **dwWidth** del [**\_ encabezado DDS**](dds-header.md) especifica el tamaño de la textura. Normalmente, se establece el miembro **dwHeight** del **\_ encabezado DDS** en 1; también se debe establecer la \_ marca de alto DDSD en el miembro **dwFlags** del **\_ encabezado DDS**.                      | 2     |
| \_TEXTURE2D de dimensión DDS \_ ( \_ dimensión de recursos D3D10 \_ \_ TEXTURE2D) | El recurso es una [textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) con un área especificada por los miembros **dwWidth** y **dwHeight** del [**\_ encabezado DDS**](dds-header.md). También puede utilizar este tipo para identificar una textura de mapa de cubo. Para obtener más información sobre cómo identificar una textura de mapa de cubos, vea **miscFlag** y **tamaño** members. | 3     |
| \_TEXTURE3D de dimensión DDS \_ ( \_ dimensión de recursos D3D10 \_ \_ TEXTURE3D) | El recurso es una [textura 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) con un volumen especificado por los miembros **dwWidth**, **DwHeight** y **dwDepth** del [**\_ encabezado DDS**](dds-header.md). También debe establecer la marca de \_ profundidad DDSD en el miembro **dwFlags** del **\_ encabezado DDS**.                                                                   | 4     |



 

</dd> <dt>

**miscFlag**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Identifica otras opciones menos comunes para los recursos. El siguiente valor para este miembro es un subconjunto de los valores de [**la \_ \_ \_ marca de recurso D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) o de la enumeración de [**\_ \_ varios \_ recursos D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) :



| Tipo                             | Descripción                                                                                                  | Value |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| \_TEXTURECUBE de recursos DDS \_ \_ | Indica que una [textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) es una textura de mapa de cubo. | 0x4   |



 

</dd> <dt>

**Tamaño**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de elementos de la matriz.

En el caso de una [textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) que también sea una textura de mapa de cubos, este número representa el número de cubos. Este número es el mismo que el número del miembro **NumCubes** de [**D3D10 \_ TEXCUBE \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) o [**D3D11 \_ TEXCUBE \_ array \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)). En este caso, el archivo DDS contiene  \* texturas de tamaño 6 2D. Para obtener más información sobre este caso, vea la descripción de **miscFlag** .

En el caso de una [textura 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), debe establecer este número en 1.

</dd> <dt>

**miscFlags2**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Contiene metadatos adicionales (antes estaba reservado). Los 3 bits inferiores indican el modo alfa del recurso asociado. Los 29 bits superiores están reservados y normalmente son 0.



| Tipo                            | Descripción                                                                                                                              | Value |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| \_modo Alpha de DDS \_ \_ desconocido       | Se desconoce el contenido del canal alfa. Este es el valor de los archivos heredados, que normalmente se supone que es una alfa "recta".                 | 0x0   |
| \_modo Alpha de DDS \_ \_ recto      | Se supone que todo el contenido del canal alfa usa alfa recto.                                                                             | 0x1   |
| \_PREmultiplicado en modo alfa DDS \_ \_ | Cualquier contenido de canal alfa usa alfa premultiplicado. Los únicos formatos de archivo heredados que indican que esta información son "DX2" y "DX4". | 0x2   |
| \_modo Alpha de DDS \_ \_ opaco        | Todo el contenido del canal alfa se establece en totalmente opaco.                                                                                    | 0x3   |
| \_modo Alpha de DDS \_ \_ personalizado        | Cualquier contenido de canal alfa se utiliza como cuarto canal y no se ha diseñado para representar la transparencia (directa o premultiplicada).      | 0x4   |



 

> [!Note]  
> Las bibliotecas de utilidades de D3DX 10 y [d3dx 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) heredadas no podrán cargar ninguno. El archivo DDS con **miscFlags2** no es igual a cero.

 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use esta estructura junto con un [**\_ encabezado DDS**](dds-header.md) para almacenar una matriz de recursos en un archivo DDS. Para obtener más información, consulte [matrices de texturas](dx-graphics-dds-pguide.md).

Este encabezado está presente si el miembro **dwFourCC** de la estructura de [**\_ PIXELFORMAT de DDS**](dds-pixelformat.md) se establece en ' contenido DX10 '.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

