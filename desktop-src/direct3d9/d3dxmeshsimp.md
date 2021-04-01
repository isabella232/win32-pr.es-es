---
description: Especifica las opciones de simplificación para una malla.
ms.assetid: f03170bd-7d2a-4839-9aec-c29426b95437
title: Enumeración D3DXMESHSIMP (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHSIMP
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: faf4244d115076b6b04cd04697acf789172d9b11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157180"
---
# <a name="d3dxmeshsimp-enumeration"></a>Enumeración D3DXMESHSIMP

Especifica las opciones de simplificación para una malla.

## <a name="syntax"></a>Sintaxis


```C++
enum _D3DXMESHSIMP {
  D3DXMESHSIMP_VERTEX  = 1, 
  D3DXMESHSIMP_FACE    = 2 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**\_Vértice D3DXMESHSIMP**
</dt> <dd>

La malla se simplificará según el número de vértices especificado en el parámetro MinValue.

</dd> <dt>

<span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP \_**
</dt> <dd>

La malla se simplificará según el número de caras especificadas en el parámetro MinValue.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 




