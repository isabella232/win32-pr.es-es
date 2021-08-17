---
description: Define el estilo de transición entre los valores de una animación de malla.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: D3DXTRANSITION_TYPE enumeración (D3dx9anim.h)
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
ms.openlocfilehash: f451b94fe204a82cd15c65e424cc214025aa670f82af5224897100cbc6f8f6e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730942"
---
# <a name="d3dxtransition_type-enumeration"></a>Enumeración D3DXTRANSITION \_ TYPE

Define el estilo de transición entre los valores de una animación de malla.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ LINEAR**
</dt> <dd>

Transición lineal entre valores.

</dd> <dt>

<span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ EASEINEASEOUT**
</dt> <dd>

Transición spline de fácil entrada y salida entre valores.

</dd> <dt>

<span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase a un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El cálculo de la rampa de la facilidad de entrada a la salida se calcula de la siguiente manera:

<dl> Q(t) = 2(x - y)t así + 3(y - x)t además de x  
</dl>

donde la rampa es una función Q(t) con las siguientes propiedades:

-   Q(t) es una spline cúbica.
-   Q(t) interpola entre x e y como intervalos t de 0 a 1.
-   Q(t) es horizontal cuando t = 0 y t = 1.

Matemáticamente, esto se traduce en:

<dl> Q(t) = At'+ Bt' + Ct + D (y, por lo tanto, Q'(t) = 3Atincompatibilidad + 2Bt + C)  
2a) Q(0) = x  
2b) Q(1) = y  
3a) Q'(0) = 0  
3b) Q'(1) = 0  
</dl>

Solución de A, B, C, D:

<dl> D = x (de 2a)  
C = 0 (de 3a)  
3A + 2B = 0 (de 3b)  
A + B = y - x (de 2b y D = x)  
</dl>

Por lo tanto:

<dl> A = 2(x - y), B = 3(y - x), C = 0, D = x  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




