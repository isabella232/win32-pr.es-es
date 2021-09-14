---
description: 'Estructura D3DXPLANE (D3dx9math.h): describe un plano.'
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: Estructura D3DXPLANE (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 3df0c94dbd49cf38d9230a2c5392df8497c64761
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970860"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a>Estructura D3DXPLANE (D3dx9math.h)

Describe un plano.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a>Members

<dl> <dt>

**Un**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coeficiente del plano de recorte en la ecuación de plano general. Vea la sección Comentarios.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coeficiente b del plano de recorte en la ecuación de plano general. Vea la sección Comentarios.

</dd> <dt>

**c**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coeficiente c del plano de recorte en la ecuación de plano general. Vea la sección Comentarios.

</dd> <dt>

**d**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Coeficiente d del plano de recorte en la ecuación del plano general. Vea la sección Comentarios.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los miembros de la **estructura D3DXPLANE** toman la forma de la ecuación de plano general. Encajan en la ecuación del plano general para que **x**+ **b** y + **c** z + **d** w = 0.

Los programadores de C++ pueden aprovechar la sobrecarga de operadores y la conversión de tipos con las extensiones [**D3DXPLANE**](d3dxplane-extensions.md) que implementan constructores sobrecargados y operadores de asignación, unario y binario (incluida la igualdad).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
