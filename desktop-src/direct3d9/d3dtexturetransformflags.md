---
description: Define valores de transformación de coordenadas de textura.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: Enumeración D3DTEXTURETRANSFORMFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 63426c0d57dee02823ee2f37327ba7c66d421b24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280261"
---
# <a name="d3dtexturetransformflags-enumeration"></a>Enumeración D3DTEXTURETRANSFORMFLAGS

Define valores de transformación de coordenadas de textura.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**Deshabilitación de D3DTTFF \_**
</dt> <dd>

Las coordenadas de textura se pasan directamente al rasterizador.

</dd> <dt>

<span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**
</dt> <dd>

El rasterizador debería esperar coordenadas de textura 1D. Este valor lo utiliza el procesamiento de vértices de función fija; debe establecerse en 0 cuando se usa un sombreador de vértices programable.

</dd> <dt>

<span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**
</dt> <dd>

El rasterizador debería esperar coordenadas de textura 2D. Este valor lo utiliza el procesamiento de vértices de función fija; debe establecerse en 0 cuando se usa un sombreador de vértices programable.

</dd> <dt>

<span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**
</dt> <dd>

El rasterizador debería esperar coordenadas de textura 3D. Este valor lo utiliza el procesamiento de vértices de función fija; debe establecerse en 0 cuando se usa un sombreador de vértices programable.

</dd> <dt>

<span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**
</dt> <dd>

El rasterizador debería esperar 4D coordenadas de textura. Este valor lo utiliza el procesamiento de vértices de función fija; debe establecerse en 0 cuando se usa un sombreador de vértices programable.

</dd> <dt>

<span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ previsto**
</dt> <dd>

Esta marca se respeta por la canalización de píxeles de función fija, así como por la canalización de píxeles programable en las versiones PS 1 \_ \_ a PS \_ 1 \_ 3. Cuando se habilita la proyección de textura para una fase de textura, los cuatro valores de punto flotante se deben escribir en el registro de textura correspondiente. Cada coordenada de textura se divide por el último elemento antes de pasarla al rasterizador. Por ejemplo, si se especifica esta marca con la \_ marca D3DTTFF COUNT3, las coordenadas de textura primera y segunda se dividen por la tercera coordenada antes de pasarse al rasterizador.

</dd> <dt>

<span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las coordenadas de textura se pueden transformar mediante una matriz de 4 x 4 antes de que los resultados se pasen al rasterizador. Las transformaciones de coordenadas de textura se establecen mediante una llamada a [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api)y pasando el \_ Estado de fase de textura D3DTSS TEXTURETRANSFORMFLAGS y uno de los valores de **D3DTEXTURETRANSFORMFLAGS**. Para obtener más información sobre las transformaciones de textura, vea [transformaciones de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
