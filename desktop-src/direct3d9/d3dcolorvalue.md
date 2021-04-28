---
description: 'Estructura D3DCOLORVALUE (D3D9Types.h): describe los valores de color.'
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: Estructura D3DCOLORVALUE (D3D9Types.h)
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
ms.openlocfilehash: c9b55fbf718382e9dca7e3999cce0cabe895a261
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116063"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a>Estructura D3DCOLORVALUE (D3D9Types.h)

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

Valor de punto flotante que especifica el componente rojo de un color. Este valor suele estar en el intervalo de 0,0 a 1,0. Un valor de 0,0 indica la ausencia completa del componente rojo, mientras que un valor de 1,0 indica que el rojo está totalmente presente.

</dd> <dt>

**g**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de punto flotante que especifica el componente verde de un color. Este valor suele estar en el intervalo de 0,0 a 1,0. Un valor de 0,0 indica la ausencia completa del componente verde, mientras que un valor de 1,0 indica que el verde está totalmente presente.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de punto flotante que especifica el componente azul de un color. Este valor suele estar en el intervalo de 0,0 a 1,0. Un valor de 0,0 indica la ausencia completa del componente azul, mientras que un valor de 1,0 indica que el azul está totalmente presente.

</dd> <dt>

**Un**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de punto flotante que especifica el componente alfa de un color. Este valor suele estar en el intervalo de 0,0 a 1,0. Un valor de 0,0 indica totalmente transparente, mientras que un valor de 1,0 indica totalmente opaco.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puede establecer los miembros de esta estructura en valores fuera del intervalo de 0 a 1 para implementar algunos efectos inusuales. Los valores mayores que 1 producen luces fuertes que tienden a apagar una escena. Los valores negativos generan luces oscuras que realmente quitan la luz de una escena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




