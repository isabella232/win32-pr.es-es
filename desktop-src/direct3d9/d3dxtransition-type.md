---
description: Define el estilo de transición entre los valores de una animación de malla.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: Enumeración D3DXTRANSITION_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ca6ef7f9dcee8e865a1cd4089aecd1bc239d5d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003804"
---
# <a name="d3dxtransition_type-enumeration"></a>\_Enumeración de tipo D3DXTRANSITION

Define el estilo de transición entre los valores de una animación de malla.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**\_Lineal D3DXTRANSITION**
</dt> <dd>

Transición lineal entre valores.

</dd> <dt>

<span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ EASEINEASEOUT**
</dt> <dd>

Aceleración de la transición spline de fácil entrada entre valores.

</dd> <dt>

<span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El cálculo de la rampa de la entrada lenta a la salida se calcula de la manera siguiente:

<dl> Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x  
</dl>

donde la rampa es una función Q (t) con las siguientes propiedades:

-   Q (t) es una spline cúbica.
-   Q (t) se interpola entre x e y como t oscila entre 0 y 1.
-   Q (t) es horizontal cuando t = 0 y t = 1.

Matemáticamente, esto se traduce en:

<dl> Q (t) = at ³ + BT ² + CT + D (y, por lo tanto, Q ' (t) = 3At ² + 2Bt + C)  
2A) Q (0) = x  
2B) Q (1) = y  
3A) Q ' (0) = 0  
3B) Q ' (1) = 0  
</dl>

Resolver para A, B, C, D:

<dl> D = x (desde 2A)  
C = 0 (de 3A)  
3A + 2B = 0 (de 3B)  
A + B = y-x (de 2B y D = x)  
</dl>

Por lo tanto:

<dl> A = 2 (x-y), B = 3 (y-x), C = 0, D = x  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




