---
description: Define las funciones de comparación admitidas.
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: Enumeración D3DCMPFUNC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCMPFUNC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e49f0e058e795e00349020619f1e6d6310dfd94f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914709"
---
# <a name="d3dcmpfunc-enumeration"></a>Enumeración D3DCMPFUNC

Define las funciones de comparación admitidas.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DCMPFUNC { 
  D3DCMP_NEVER         = 1,
  D3DCMP_LESS          = 2,
  D3DCMP_EQUAL         = 3,
  D3DCMP_LESSEQUAL     = 4,
  D3DCMP_GREATER       = 5,
  D3DCMP_NOTEQUAL      = 6,
  D3DCMP_GREATEREQUAL  = 7,
  D3DCMP_ALWAYS        = 8,
  D3DCMP_FORCE_DWORD   = 0x7fffffff
} D3DCMPFUNC, *LPD3DCMPFUNC;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ nunca**
</dt> <dd>

Siempre produce un error en la prueba.

</dd> <dt>

<span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ menos**
</dt> <dd>

Acepte el nuevo píxel si su valor es menor que el valor del píxel actual.

</dd> <dt>

<span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**Igual a D3DCMP \_**
</dt> <dd>

Acepte el nuevo píxel si su valor es igual al valor del píxel actual.

</dd> <dt>

<span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP \_ LESSEQUAL**
</dt> <dd>

Acepte el nuevo píxel si su valor es menor o igual que el valor del píxel actual.

</dd> <dt>

<span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_ mayor**
</dt> <dd>

Acepte el nuevo píxel si su valor es mayor que el valor del píxel actual.

</dd> <dt>

<span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**\_NOTEQUAL D3DCMP**
</dt> <dd>

Acepte el nuevo píxel si su valor no es igual al valor del píxel actual.

</dd> <dt>

<span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP \_ mayor criticalthreshold**
</dt> <dd>

Acepte el nuevo píxel si su valor es mayor o igual que el valor del píxel actual.

</dd> <dt>

<span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP \_ siempre**
</dt> <dd>

Pase siempre la prueba.

</dd> <dt>

<span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores de este tipo enumerado definen las funciones de comparación admitidas para los \_ Estados de representación D3DRS ZFUNC, D3DRS \_ ALPHAFUNC y D3DRS \_ STENCILFUNC.

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

 

 
