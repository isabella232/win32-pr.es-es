---
description: Define opciones para realizar cálculos de distancia geodésica, al ajustar una textura a una superficie curva. Use esta marca para elegir entre cálculos rápidos y de alta calidad al calcular un atlas de textura.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: Enumeración D3DCOREVATLAS (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 64cc116199b688fc9dcd8d6fbf331d85da508948
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566080"
---
# <a name="d3dxuvatlas-enumeration"></a>D3DVATVATLAS (enumeración)

Define opciones para realizar cálculos de distancia geodésica, al ajustar una textura a una superficie curva. Use esta marca para elegir entre cálculos rápidos y de alta calidad al calcular un atlas de textura.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DVATVATLAS \_ PREDETERMINADO**
</dt> <dd>

Las mallas con más de 25 000 caras tendrán aplicado el método de distancia geodésica rápida, mientras que las mallas con menos de 25 000 caras tendrán aplicado el método de distancia geodésica de mayor calidad.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DVATVATLAS \_ GEODESIC \_ FAST**
</dt> <dd>

Usa aproximaciones para mejorar la velocidad de gráficos a costa de que se agregan gráficos extendidos o más para la malla.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**CALIDAD \_ GEODÉSICA DE D3DVATLAS \_**
</dt> <dd>

Proporciona gráficos de mejor calidad, pero requiere más tiempo y memoria que rapidez.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




