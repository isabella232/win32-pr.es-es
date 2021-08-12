---
title: DDS_HEADER_DXT10 estructura (Dds.h)
description: Extensión de encabezado DDS para controlar matrices de recursos, formatos de píxel DXGI que no se asignan a las estructuras de formato de píxel de Microsoft DirectDraw heredadas y metadatos adicionales.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- DDS_HEADER_DXT10 DDS de estructura
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
ms.openlocfilehash: 9da95b65739922861002ab134d33f276adabd19c29d14fdea6432616b6c5edc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289792"
---
# <a name="dds_header_dxt10-structure"></a>DDS \_ HEADER \_ DXT10 (estructura)

Extensión de encabezado DDS para controlar matrices de recursos, formatos de píxel DXGI que no se asignan a las estructuras de formato de píxel de Microsoft DirectDraw heredadas y metadatos adicionales.

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

Tipo: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

El formato de píxel de superficie (vea [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

</dd> <dt>

**resourceDimension**
</dt> <dd>

Tipo: **[ **DIMENSIÓN DE \_ RECURSOS \_ D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Identifica el tipo de recurso. Los valores siguientes para este miembro son un subconjunto de los valores de la enumeración [**\_ RESOURCE \_ DIMENSION de D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) o [**RESOURCE \_ \_ DIMENSION D3D11:**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension)



| Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                            | Valor |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| DIMENSIÓN DE DDS \_ \_ TEXTURE1D (D3D10 \_ RESOURCE \_ DIMENSION \_ TEXTURE1D) | El recurso es una [textura 1D.](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) El **miembro dwWidth** de [**DDS \_ HEADER**](dds-header.md) especifica el tamaño de la textura. Normalmente, el miembro **dwHeight** de **DDS \_ HEADER** se establece en 1; también debe establecer la marca HEIGHT de DDSD en el miembro \_ **dwFlags** de **DDS \_ HEADER**.                      | 2     |
| DIMENSIÓN DE DDS \_ \_ TEXTURE2D (D3D10 \_ RESOURCE \_ DIMENSION \_ TEXTURE2D) | El recurso es [una textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) con un área especificada por los **miembros dwWidth** y **dwHeight** de [**DDS \_ HEADER**](dds-header.md). También puede usar este tipo para identificar una textura de mapa de cubo. Para obtener más información sobre cómo identificar una textura de mapa de cubo, vea **miscFlag** y **arraySize** members. | 3     |
| DIMENSIÓN DE DDS \_ \_ TEXTURE3D (D3D10 \_ RESOURCE \_ DIMENSION \_ TEXTURE3D) | El recurso es [una textura 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) con un volumen especificado por los miembros **dwWidth**, **dwHeight** y **dwDepth** de [**los miembros DDS \_ HEADER**](dds-header.md). También debe establecer la marca DDSD \_ DEPTH en el miembro **dwFlags** de **DDS \_ HEADER**.                                                                   | 4     |



 

</dd> <dt>

**miscFlag**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Identifica otras opciones menos comunes para los recursos. El siguiente valor para este miembro es un subconjunto de los valores de la enumeración [**\_ \_ MISC \_ FLAG de RECURSOS D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) o [**D3D11 \_ RESOURCE \_ MISC \_ FLAG:**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)



| Tipo                             | Descripción                                                                                                  | Valor |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| RESOURCE \_ \_ MISC \_ TEXTURECUBE DE DDS | Indica que una [textura 2D es](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) una textura de mapa de cubo. | 0x4   |



 

</dd> <dt>

**arraySize**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de elementos de la matriz.

Para una [textura 2D que](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) también es una textura de mapa de cubo, este número representa el número de cubos. Este número es el mismo que el número del miembro **NumCubes** de [**D3D10 \_ TEXCUBE \_ ARRAY \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) o [**D3D11 \_ TEXCUBE \_ ARRAY \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)). En este caso, el archivo DDS contiene **texturas arraySize** \* 6 2D. Para obtener más información sobre este caso, vea **la descripción de miscFlag.**

Para una [textura 3D,](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)debe establecer este número en 1.

</dd> <dt>

**miscFlags2**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Contiene metadatos adicionales (anteriormente estaba reservado). Los 3 bits inferiores indican el modo alfa del recurso asociado. Los 29 bits superiores están reservados y suelen ser 0.



| Tipo                            | Descripción                                                                                                                              | Valor |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| MODO ALFA DE DDS \_ \_ \_ DESCONOCIDO       | Se desconoce el contenido del canal alfa. Este es el valor de los archivos heredados, que normalmente se supone que son alfa "directos".                 | 0x0   |
| MODO ALFA DE DDS \_ \_ \_ DIRECTO      | Se supone que cualquier contenido de canal alfa usa alfa recta.                                                                             | 0x1   |
| MODO ALFA DDS \_ \_ \_ PREMULTIPLICADO | Cualquier contenido de canal alfa usa alfa premultiplicado. Los únicos formatos de archivo heredados que indican esta información son "DX2" y "DX4". | 0x2   |
| DDS \_ ALPHA \_ MODE \_ OPAQUE        | Todo el contenido del canal alfa está establecido en totalmente opaco.                                                                                    | 0x3   |
| MODO ALFA DE DDS \_ \_ \_ PERSONALIZADO        | Cualquier contenido de canal alfa se usa como un 4º canal y no está diseñado para representar la transparencia (recta o premultiplicada).      | 0x4   |



 

> [!Note]  
> Las bibliotecas de utilidades D3DX 10 y [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) heredadas no podrán cargar ningún . El archivo DDS **con miscFlags2 no** es igual a cero.

 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Use esta estructura junto con un [**encabezado DDS \_ para**](dds-header.md) almacenar una matriz de recursos en un archivo DDS. Para obtener más información, vea [matrices de textura.](dx-graphics-dds-pguide.md)

Este encabezado está presente si el **miembro dwFourCC** de la estructura [**\_ PIXELFORMAT de DDS**](dds-pixelformat.md) está establecido en "DX10".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dds.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Referencia de DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

