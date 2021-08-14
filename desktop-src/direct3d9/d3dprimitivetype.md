---
description: Define las primitivas admitidas por Direct3D.
ms.assetid: 89e697f9-02b9-4ae1-9e86-6178da0cb008
title: Enumeración D3DPRIMITIVETYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRIMITIVETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a7406670b055a11f30a71677a88dc6230aecec8d7660d886b1d63f53e6e61566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527521"
---
# <a name="d3dprimitivetype-enumeration"></a>D3DPRIMITIVETYPE (enumeración)

Define las primitivas admitidas por Direct3D.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DPRIMITIVETYPE { 
  D3DPT_POINTLIST      = 1,
  D3DPT_LINELIST       = 2,
  D3DPT_LINESTRIP      = 3,
  D3DPT_TRIANGLELIST   = 4,
  D3DPT_TRIANGLESTRIP  = 5,
  D3DPT_TRIANGLEFAN    = 6,
  D3DPT_FORCE_DWORD    = 0x7fffffff
} D3DPRIMITIVETYPE, *LPD3DPRIMITIVETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT \_ POINTLIST**
</dt> <dd>

Representa los vértices como una colección de puntos aislados. Este valor no se admite para las primitivas indizadas.

</dd> <dt>

<span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT \_ LINELIST**
</dt> <dd>

Representa los vértices como una lista de segmentos de línea recta aislados.

</dd> <dt>

<span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT \_ LINESTRIP**
</dt> <dd>

Representa los vértices como una sola polilínea.

</dd> <dt>

<span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT \_ TRIANGLELIST**
</dt> <dd>

Representa los vértices especificados como una secuencia de triángulos aislados. Cada grupo de tres vértices define un triángulo independiente.

La selección de la cara posterior se ve afectada por el estado de representación del orden de sinuoso actual.

</dd> <dt>

<span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT \_ TRIANGLESTRIP**
</dt> <dd>

Representa los vértices como una franja de triángulo. La marca de selección de cara posterior se volteará automáticamente en triángulos numerados uniformemente.

</dd> <dt>

<span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT \_ TRIANGLEFAN**
</dt> <dd>

Representa los vértices como un ventilador de triángulo.

</dd> <dt>

<span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El [uso de franjas de](triangle-strips.md) triángulo o ventiladores de triángulo [(Direct3D 9)](triangle-fans.md) suele ser más eficaz que usar listas de triángulos porque se duplican menos vértices.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::D rawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)
</dt> <dt>

[**IDirect3DDevice9::D rawIndexedPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)
</dt> <dt>

[**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
</dt> <dt>

[**IDirect3DDevice9::D rawPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
</dt> </dl>

 

 
