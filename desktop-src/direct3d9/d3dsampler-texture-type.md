---
description: Define los tipos de textura del muestreador para los sombreadores de vértices.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: D3DSAMPLER_TEXTURE_TYPE enumeración (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 5b1755f97ad39a5924367747199cf21c1c46a209a8202cc6b38ef22c73e8ccec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408235"
---
# <a name="d3dsampler_texture_type-enumeration"></a>Enumeración D3DSAMPLER \_ TEXTURE \_ TYPE

Define los tipos de textura del muestreador para los sombreadores de vértices.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ UNKNOWN**
</dt> <dd>

Valor no inicializado. El valor de este elemento es 0 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT.

</dd> <dt>

<span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**
</dt> <dd>

Declarar una textura 2D. El valor de este elemento es 2 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT.

</dd> <dt>

<span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**CUBO D3DSTT \_**
</dt> <dd>

Declarar una textura de cubo. El valor de este elemento es &lt; &lt; 3 D3DSP \_ TEXTURETYPE \_ SHIFT.

</dd> <dt>

<span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**D3DSTT \_ VOLUME**
</dt> <dd>

Declarar una textura de volumen. El valor de este elemento es 4 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT.

</dd> <dt>

<span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




