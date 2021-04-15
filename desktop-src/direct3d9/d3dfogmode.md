---
description: Define constantes que describen el modo de niebla.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: Enumeración D3DFOGMODE (D3D9Types. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362647"
---
# <a name="d3dfogmode-enumeration"></a>Enumeración D3DFOGMODE

Define constantes que describen el modo de niebla.

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

<span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ ninguno**
</dt> <dd>

Ningún efecto de niebla.

</dd> <dt>

<span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ exp**
</dt> <dd>

El efecto de niebla se intensifica exponencialmente, de acuerdo con la siguiente fórmula.

![fórmula de intensidad del efecto niebla](images/fogexp.png)

</dd> <dt>

<span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**
</dt> <dd>

El efecto de niebla intensifica exponencialmente con el cuadrado de la distancia, de acuerdo con la siguiente fórmula.

![fórmula de intensidad del efecto niebla basada en el cuadrado de la distancia](images/fogexp2.png)

</dd> <dt>

<span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**\_Lineal D3DFOG**
</dt> <dd>

El efecto de niebla intensifica linealmente entre los puntos inicial y final, de acuerdo con la siguiente fórmula.

![fórmula de intensidad del efecto niebla basada en los puntos inicial y final](images/fogliner.png)

Este es el único modo de niebla compatible actualmente.

</dd> <dt>

<span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores de este tipo enumerado se usan en los \_ Estados de representación D3DRS FOGTABLEMODE y D3DRS \_ FOGVERTEXMODE.

La niebla se puede considerar una medida de visibilidad: cuanto menor sea el valor de niebla producido por una ecuación de niebla, menos visible será un objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
