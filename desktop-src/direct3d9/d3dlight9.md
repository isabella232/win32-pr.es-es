---
description: Define un conjunto de propiedades de iluminación.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: Estructura D3DLIGHT9 (D3D9Types. h)
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
ms.openlocfilehash: 90e72fbb2bf4f1d74a74dc177346387b36eb25e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280375"
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

Tipo de la fuente de luz. Este valor es uno de los miembros del tipo enumerado [**D3DLIGHTTYPE**](./d3dlighttype.md) .

</dd> <dt>

**Difusa**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Color difuso emitido por la luz. Este miembro es una estructura [**D3DCOLORVALUE**](d3dcolorvalue.md) .

</dd> <dt>

**Especular**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Color especular emitido por la luz. Este miembro es una estructura [**D3DCOLORVALUE**](d3dcolorvalue.md) .

</dd> <dt>

**Ambiente**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Color ambiente emitido por la luz. Este miembro es una estructura [**D3DCOLORVALUE**](d3dcolorvalue.md) .

</dd> <dt>

**Position**
</dt> <dd>

Tipo: **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Posición de la luz en el espacio universal, especificada por una estructura [**D3DVECTOR**](d3dvector.md) . Este miembro no tiene ningún significado para las luces direccionales y se omite en ese caso.

</dd> <dt>

**Dirección**
</dt> <dd>

Tipo: **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Dirección en la que apunta la luz en el espacio universal, especificado por una estructura [**D3DVECTOR**](d3dvector.md) . Este miembro solo tiene significado para direccional y Spotlight. No es necesario normalizar este vector, pero debe tener una longitud que no sea cero.

</dd> <dt>

**Range**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Distancia más allá de la cual la luz no tiene ningún efecto. El valor máximo permitido para este miembro es la raíz cuadrada de FLT \_ máx. Este miembro no afecta a las luces direccionales.

</dd> <dt>

**Disminución**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Disminuya la iluminación entre el cono interior de un foco (el ángulo especificado por Theta) y el borde exterior del cono exterior (el ángulo especificado por la PHI).

El efecto de la caída en la iluminación es sutil. Además, se incurre en una pequeña reducción del rendimiento dando forma a la curva de difuminación. Por estos motivos, la mayoría de los desarrolladores establecen este valor en 1,0.

</dd> <dt>

**Attenuation0**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor que especifica cómo cambia la intensidad de la luz con la distancia. Los valores de atenuación se omiten para las luces direccionales. Este miembro representa una constante de atenuación. Para obtener información sobre la atenuación, consulte [propiedades de luz (Direct3D 9)](light-properties.md). Valores válidos para este intervalo de miembros de 0,0 a infinito. En el caso de las luces no direccionales, los tres valores de atenuación no deben establecerse en 0,0 al mismo tiempo.

</dd> <dt>

**Attenuation1**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor que especifica cómo cambia la intensidad de la luz con la distancia. Los valores de atenuación se omiten para las luces direccionales. Este miembro representa una constante de atenuación. Para obtener información sobre la atenuación, consulte [propiedades de luz (Direct3D 9)](light-properties.md). Valores válidos para este intervalo de miembros de 0,0 a infinito. En el caso de las luces no direccionales, los tres valores de atenuación no deben establecerse en 0,0 al mismo tiempo.

</dd> <dt>

**Attenuation2**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor que especifica cómo cambia la intensidad de la luz con la distancia. Los valores de atenuación se omiten para las luces direccionales. Este miembro representa una constante de atenuación. Para obtener información sobre la atenuación, consulte [propiedades de luz (Direct3D 9)](light-properties.md). Valores válidos para este intervalo de miembros de 0,0 a infinito. En el caso de las luces no direccionales, los tres valores de atenuación no deben establecerse en 0,0 al mismo tiempo.

</dd> <dt>

**Zeta**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Ángulo, en radianes, del cono interior de un foco, es decir, el cono de foco de luz completamente iluminado. Este valor debe estar en el intervalo comprendido entre 0 y el valor especificado por Phi.

</dd> <dt>

**Su**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Ángulo, en radianes, que define el borde exterior del cono exterior del foco. Los puntos fuera de este cono no están iluminados por el foco. Este valor debe estar comprendido entre 0 y PI.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[**SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
