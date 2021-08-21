---
description: Define un conjunto de propiedades de iluminación.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: Estructura D3DLIGHT9 (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e38cd5b6cfaba4822ddecf121aa2b03c86e2a3a899e464df18bfa473322f41f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804842"
---
# <a name="d3dlight9-structure"></a>Estructura D3DLIGHT9

Define un conjunto de propiedades de iluminación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**

</dd> <dd>

Tipo de la fuente de luz. Este valor es uno de los miembros del tipo enumerado [**D3DLIGHTTYPE.**](./d3dlighttype.md)

</dd> <dt>

**Difusa**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Color difuso emitido por la luz. Este miembro es una [**estructura D3DCOLORVALUE.**](d3dcolorvalue.md)

</dd> <dt>

**Especular**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Color especular emitido por la luz. Este miembro es una [**estructura D3DCOLORVALUE.**](d3dcolorvalue.md)

</dd> <dt>

**Ambiente**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Color ambiente emitido por la luz. Este miembro es una [**estructura D3DCOLORVALUE.**](d3dcolorvalue.md)

</dd> <dt>

**Position**
</dt> <dd>

Tipo: **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Posición de la luz en el espacio mundial, especificada por una [**estructura D3DVECTOR.**](d3dvector.md) Este miembro no tiene ningún significado para las luces direccionales y se omite en ese caso.

</dd> <dt>

**Dirección**
</dt> <dd>

Tipo: **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Dirección en la que la luz apunta al espacio mundial, especificado por una [**estructura D3DVECTOR.**](d3dvector.md) Este miembro solo tiene significado para los focos direccionales y . No es necesario normalizar este vector, pero debe tener una longitud distinta de cero.

</dd> <dt>

**Intervalo**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Distancia más allá de la cual la luz no tiene ningún efecto. El valor máximo permitido para este miembro es la raíz cuadrada de FLT \_ MAX. Este miembro no afecta a las luces direccionales.

</dd> <dt>

**Difuminación**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Disminución de la iluminación entre el cono interno de un foco (el ángulo especificado por Theta) y el borde exterior del cono exterior (el ángulo especificado por Phi).

El efecto de la caída en la iluminación es sutil. Además, se incurre en una pequeña penalización del rendimiento al dar forma a la curva de reserva. Por estos motivos, la mayoría de los desarrolladores establecen este valor en 1.0.

</dd> <dt>

**Atenuación0**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor que especifica cómo cambia la intensidad de la luz a lo largo de la distancia. Los valores de atenuación se omiten para las luces direccionales. Este miembro representa una constante de atenuación. Para obtener información sobre la atenuación, vea [Propiedades de luz (Direct3D 9).](light-properties.md) Los valores válidos para este miembro van de 0,0 a infinito. En el caso de las luces no direccionales, los tres valores de atenuación no deben establecerse en 0,0 al mismo tiempo.

</dd> <dt>

**Atenuación1**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor que especifica cómo cambia la intensidad de la luz a lo largo de la distancia. Los valores de atenuación se omiten para las luces direccionales. Este miembro representa una constante de atenuación. Para obtener información sobre la atenuación, vea [Propiedades de luz (Direct3D 9).](light-properties.md) Los valores válidos para este miembro van de 0,0 a infinito. En el caso de las luces no direccionales, los tres valores de atenuación no deben establecerse en 0,0 al mismo tiempo.

</dd> <dt>

**Atenuación2**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor que especifica cómo cambia la intensidad de la luz a lo largo de la distancia. Los valores de atenuación se omiten para las luces direccionales. Este miembro representa una constante de atenuación. Para obtener información sobre la atenuación, vea [Propiedades de luz (Direct3D 9).](light-properties.md) Los valores válidos para este miembro van de 0,0 a infinito. En el caso de las luces no direccionales, los tres valores de atenuación no deben establecerse en 0,0 al mismo tiempo.

</dd> <dt>

**Theta**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Ángulo, en radianes, del cono interno de un foco, es decir, el cono de foco completamente iluminado. Este valor debe estar en el intervalo entre 0 y el valor especificado por Phi.

</dd> <dt>

**Phi**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Ángulo, en radianes, que define el borde exterior del cono exterior del foco. Los puntos fuera de este cono no están encendidos por el foco. Este valor debe estar entre 0 y pi.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[**SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
