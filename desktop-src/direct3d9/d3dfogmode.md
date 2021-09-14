---
description: Define constantes que describen el modo Desenlaz.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: Enumeración D3DFOGMODE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8436a52edbb9460c6945c1526513629939ec444b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963772"
---
# <a name="d3dfogmode-enumeration"></a>D3DFOGMODE (enumeración)

Define constantes que describen el modo Desenlaz.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ NONE**
</dt> <dd>

Ningún efecto de efecto de

</dd> <dt>

<span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ EXP**
</dt> <dd>

El efecto de efecto de efecto de efecto de efecto se incrementa exponencialmente, según la fórmula siguiente.

![fórmula de intensidad de efecto de nube](images/fogexp.png)

</dd> <dt>

<span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**
</dt> <dd>

El efecto de efecto de efecto de efecto de efecto se multiplica exponencialmente con el cuadrado de la distancia, según la fórmula siguiente.

![fórmula de intensidad de efecto de nube basada en el cuadrado de distancia](images/fogexp2.png)

</dd> <dt>

<span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG \_ LINEAR**
</dt> <dd>

El efecto de efecto de efecto de efecto de efecto oscila linealmente entre los puntos inicial y final, según la fórmula siguiente.

![fórmula de intensidad de efecto de lluvia en función de los puntos inicial y final](images/fogliner.png)

Este es el único modo de "mode" admitido actualmente.

</dd> <dt>

<span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los estados de representación D3DRS CONFIGURABLEMODE y \_ D3DRS CONFIGURABLEVERTEXMODE usan los valores \_ de este tipo enumerado.

La distancia se puede considerar como una medida de visibilidad: cuando menor sea el valor de lamas producido por una ecuación de cálculo, menos visible será un objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
