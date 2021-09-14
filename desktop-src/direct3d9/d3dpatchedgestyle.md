---
description: Define si el modo de teselación actual es discreto o continuo.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: Enumeración D3DPATCHEDGESTYLE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970984"
---
# <a name="d3dpatchedgestyle-enumeration"></a>D3DPATCHEDGESTYLE (enumeración)

Define si el modo de teselación actual es discreto o continuo.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ DISCRETE**
</dt> <dd>

Estilo de borde discreto. En el modo discreto, puede especificar la teselación float, pero se truncará en enteros.

</dd> <dt>

<span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ CONTINUOUS**
</dt> <dd>

Estilo de borde continuo. En el modo continuo, la teselación se especifica como valores float que se pueden variar sin problemas para reducir los artefactos de "estallido".

</dd> <dt>

<span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase a un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que la teselación continua genera un patrón de teselación completamente diferente del discreto para los mismos valores de teselación (esto es más evidente en el modo wireframe). Por lo tanto, 4.0 continuo no es lo mismo que 4 discreto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




