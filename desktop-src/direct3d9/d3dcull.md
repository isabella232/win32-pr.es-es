---
description: Define los modos de selección admitidos.
ms.assetid: b669307c-0d40-4ecb-8a2e-8bd1d9c65647
title: Enumeración D3DCULL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCULL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e88aa1baf86b2b03177cc686bf83299311065283
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707803"
---
# <a name="d3dcull-enumeration"></a>Enumeración D3DCULL

Define los modos de selección admitidos.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DCULL { 
  D3DCULL_NONE         = 1,
  D3DCULL_CW           = 2,
  D3DCULL_CCW          = 3,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DCULL, *LPD3DCULL;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL \_ ninguno**
</dt> <dd>

No revierta caras.

</dd> <dt>

<span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL \_ CW**
</dt> <dd>

Reactivar caras con vértices hacia la derecha.

</dd> <dt>

<span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL \_ CCW**
</dt> <dd>

Reactivar caras con vértices en sentido contrario a las agujas del reloj.

</dd> <dt>

<span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El estado de representación de D3DRS CULLMODE usa los valores de este tipo enumerado \_ . Los modos de selección de datos definen cómo se seleccionan los rostros al representar una geometría.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
