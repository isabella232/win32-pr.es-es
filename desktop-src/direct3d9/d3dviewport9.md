---
description: Define las dimensiones de la ventana de una superficie de representación-destino en la que se proyecta un volumen 3D.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: Estructura D3DVIEWPORT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3d96000de50934ebdc893ffc3866dd3252703bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718312"
---
# <a name="d3dviewport9-structure"></a>Estructura D3DVIEWPORT9

Define las dimensiones de la ventana de una superficie de representación-destino en la que se proyecta un volumen 3D.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a>Miembros

<dl> <dt>

**X**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada de píxeles de la esquina superior izquierda de la ventanilla en la superficie de representación-destino. A menos que desee representar en un subconjunto de la superficie, este miembro se puede establecer en 0.

</dd> <dt>

**S**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada de píxeles de la esquina superior izquierda de la ventanilla en la superficie de representación-destino. A menos que desee representar en un subconjunto de la superficie, este miembro se puede establecer en 0.

</dd> <dt>

**Width**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensión de ancho del volumen de clip, en píxeles. A menos que esté representando solo en un subconjunto de la superficie, este miembro debe establecerse en la dimensión de ancho de la superficie de representación-destino.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensión de alto del volumen de clip, en píxeles. A menos que esté representando solo en un subconjunto de la superficie, este miembro debe establecerse en la dimensión de alto de la superficie de representación-destino.

</dd> <dt>

**MinZ**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Junto con MaxZ, valor que describe el intervalo de valores de profundidad en el que se va a representar una escena, los valores mínimo y máximo del volumen de recorte. La mayoría de las aplicaciones establecen este valor en 0,0. El recorte se realiza después de aplicar la matriz de proyección.

</dd> <dt>

**MaxZ**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Junto con MinZ, valor que describe el intervalo de valores de profundidad en el que se va a representar una escena, los valores mínimo y máximo del volumen de recorte. La mayoría de las aplicaciones establecen este valor en 1,0. El recorte se realiza después de aplicar la matriz de proyección.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los miembros X, Y, ancho y alto describen la posición y las dimensiones de la ventanilla en la superficie de representación-destino. Normalmente, las aplicaciones se representan en toda la superficie de destino; Cuando se representa en una superficie de 640 x 480, estos miembros deben ser 0, 0, 640 y 480, respectivamente. MinZ y MaxZ se establecen normalmente en 0,0 y 1,0, pero se pueden establecer en otros valores para lograr efectos concretos. Por ejemplo, puede establecer ambos en 0,0 para obligar al sistema a representar objetos en el primer plano de una escena, o ambos en 1,0 para forzar los objetos en segundo plano.

Cuando los parámetros de la ventanilla para un dispositivo cambian (debido a una llamada al método [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) ), el controlador genera una nueva matriz de transformación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
