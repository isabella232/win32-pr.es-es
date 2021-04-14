---
description: Define los tipos de textura de muestra para los sombreadores de vértices.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: Enumeración D3DSAMPLER_TEXTURE_TYPE (D3D9Types. h)
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
ms.openlocfilehash: 337e8b25a8ec8389a6252fb48582128c601730ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424331"
---
# <a name="d3dsampler_texture_type-enumeration"></a>\_Enumeración de tipo de textura D3DSAMPLER \_

Define los tipos de textura de muestra para los sombreadores de vértices.

## <a name="syntax"></a>Sintaxis


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

<span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ desconocido**
</dt> <dd>

Valor sin inicializar. El valor de este elemento es 0 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.

</dd> <dt>

<span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**
</dt> <dd>

Declarar una textura 2D. El valor de este elemento es 2 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.

</dd> <dt>

<span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**\_Cubo D3DSTT**
</dt> <dd>

Declarar una textura de cubo. El valor de este elemento es 3 &lt; &lt; D3DSP de \_ TEXTURETYPE \_ .

</dd> <dt>

<span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**\_Volumen D3DSTT**
</dt> <dd>

Declarar una textura de volumen. El valor de este elemento es 4 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.

</dd> <dt>

<span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




