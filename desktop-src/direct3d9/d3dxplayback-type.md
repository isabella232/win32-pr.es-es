---
description: Define el tipo de modos de bucle de conjunto de animación usados para la reproducción.
ms.assetid: 2ce26bf0-2b33-4193-a58f-03493a051351
title: D3DXPLAYBACK_TYPE enumeración (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLAYBACK_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 642c3e1d49792016ea1d161352d4dda9fc1330aab544880e754659c735d1ecd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044793"
---
# <a name="d3dxplayback_type-enumeration"></a>D3DXPLAYBACK \_ TYPE (enumeración)

Define el tipo de modos de bucle de conjunto de animación usados para la reproducción.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXPLAYBACK_TYPE { 
  D3DXPLAY_LOOP         = 0,
  D3DXPLAY_ONCE         = 1,
  D3DXPLAY_PINGPONG     = 2,
  D3DXPLAY_FORCE_DWORD  = 0x7fffffff
} D3DXPLAYBACK_TYPE, *LPD3DXPLAYBACK_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**BUCLE \_ D3DXPLAY**
</dt> <dd>

La animación se repite sin fin.

</dd> <dt>

<span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY \_ UNA VEZ**
</dt> <dd>

La animación se reproduce una vez y, a continuación, se detiene en el último fotograma.

</dd> <dt>

<span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY \_ PINGPONG**
</dt> <dd>

La animación alterna infinitamente entre la reproducción hacia delante y la reproducción hacia atrás.

</dd> <dt>

<span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




