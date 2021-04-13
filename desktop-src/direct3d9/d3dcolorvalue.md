---
description: Describe los valores de color.
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: Estructura D3DCOLORVALUE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1fe2f187921749207bbbf51d7fcfd75357a70858
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362481"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a>Estructura D3DCOLORVALUE (D3D9Types. h)

Describe los valores de color.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**r**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de punto flotante que especifica el componente rojo de un color. Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0. Un valor de 0,0 indica la ausencia completa del componente rojo, mientras que un valor de 1,0 indica que el rojo está totalmente presente.

</dd> <dt>

**g**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de punto flotante que especifica el componente verde de un color. Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0. Un valor de 0,0 indica la ausencia completa del componente verde, mientras que un valor de 1,0 indica que el color verde está totalmente presente.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de punto flotante que especifica el componente azul de un color. Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0. Un valor de 0,0 indica la ausencia completa del componente azul, mientras que un valor de 1,0 indica que el azul está totalmente presente.

</dd> <dt>

**un**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de punto flotante que especifica el componente alfa de un color. Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0. Un valor de 0,0 indica que es completamente transparente, mientras que un valor de 1,0 indica que es totalmente opaco.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede establecer los miembros de esta estructura en valores fuera del intervalo de 0 a 1 para implementar algunos efectos inusuales. Los valores mayores que 1 producen luces fuertes que tienden a lavar una escena. Los valores negativos producen luces oscuras que realmente quitan la luz de una escena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




