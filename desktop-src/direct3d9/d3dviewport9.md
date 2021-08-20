---
description: Define las dimensiones de ventana de una superficie de destino de representación en la que se proyecta un volumen 3D.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: Estructura D3DVIEWPORT9 (D3D9Types.h)
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
ms.openlocfilehash: 40162e4350e5a68670023701f1cdae973fb8a7bac3a6d4f5c301136c4e8c2702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527271"
---
# <a name="d3dviewport9-structure"></a>D3DVIEWPORT9 (estructura)

Define las dimensiones de ventana de una superficie de destino de representación en la que se proyecta un volumen 3D.

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

Coordenada de píxeles de la esquina superior izquierda de la ventanilla en la superficie de destino de representación. A menos que desee representar en un subconjunto de la superficie, este miembro se puede establecer en 0.

</dd> <dt>

**S**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada de píxeles de la esquina superior izquierda de la ventanilla en la superficie de destino de representación. A menos que desee representar en un subconjunto de la superficie, este miembro se puede establecer en 0.

</dd> <dt>

**Width**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensión de ancho del volumen de recorte, en píxeles. A menos que se represente solo en un subconjunto de la superficie, este miembro debe establecerse en la dimensión de ancho de la superficie de destino de representación.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensión de alto del volumen de recorte, en píxeles. A menos que se represente solo en un subconjunto de la superficie, este miembro debe establecerse en la dimensión de alto de la superficie de destino de representación.

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

Junto con MinZ, valor que describe el intervalo de valores de profundidad en el que se va a representar una escena, los valores mínimo y máximo del volumen de recorte. La mayoría de las aplicaciones establecen este valor en 1.0. El recorte se realiza después de aplicar la matriz de proyección.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los miembros X, Y, Width y Height describen la posición y las dimensiones de la ventanilla en la superficie de destino de representación. Normalmente, las aplicaciones se representan en toda la superficie de destino; Cuando se representa en una superficie de 640 x 480, estos miembros deben ser 0, 0, 640 y 480, respectivamente. Las propiedades MinZ y MaxZ normalmente se establecen en 0,0 y 1,0, pero se pueden establecer en otros valores para lograr efectos específicos. Por ejemplo, puede establecer ambos en 0,0 para forzar al sistema a representar objetos en primer plano de una escena, o ambos en 1.0 para forzar los objetos en segundo plano.

Cuando cambian los parámetros de ventanilla de un dispositivo (debido a una llamada al [**método SetViewport),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) el controlador crea una nueva matriz de transformación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
