---
description: Define constantes que describen los formatos de búfer de profundidad.
ms.assetid: 5e5ce48b-8859-43e0-a9b4-5972cf6bf781
title: Enumeración D3BUFFERTYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DZBUFFERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f9a04cbc9281009ee0b270cc2dfd7b73e23a5378a2116362f63344c8d7475d7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986345"
---
# <a name="d3dzbuffertype-enumeration"></a>D3BUFFERTYPE (enumeración)

Define constantes que describen los formatos de búfer de profundidad.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DZBUFFERTYPE { 
  D3DZB_FALSE        = 0,
  D3DZB_TRUE         = 1,
  D3DZB_USEW         = 2,
  D3DZB_FORCE_DWORD  = 0x7fffffff
} D3DZBUFFERTYPE, *LPD3DZBUFFERTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3D \_ FALSE**
</dt> <dd>

Deshabilite el almacenamiento en búfer de profundidad.

</dd> <dt>

<span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3D HELL \_ TRUE**
</dt> <dd>

Habilite el almacenamiento en búfer z.

</dd> <dt>

<span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DGEL \_ USEW**
</dt> <dd>

Habilite w-buffering.

</dd> <dt>

<span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DGRAMA \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los miembros de este tipo enumerado se usan con el estado de representación ZENABLE de D3DRS. \_

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
