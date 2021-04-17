---
description: Define las opciones para realizar cálculos de distancia de poliedro, al ajustar una textura a una superficie curva. Use esta marca para elegir entre cálculos de alta calidad frente a cálculos rápidos al calcular un Atlas de textura.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: Enumeración D3DXUVATLAS (D3dx9mesh. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717700"
---
# <a name="d3dxuvatlas-enumeration"></a>Enumeración D3DXUVATLAS

Define las opciones para realizar cálculos de distancia de poliedro, al ajustar una textura a una superficie curva. Use esta marca para elegir entre cálculos de alta calidad frente a cálculos rápidos al calcular un Atlas de textura.

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

<span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**\_Valor predeterminado de D3DXUVATLAS**
</dt> <dd>

En su lugar, las mallas con más de 25.000 caras tendrán aplicado el método de distancia geodasic rápido, mientras que las mallas con menos de 25.000 caras tendrán aplicado el método de distancia de Poliedro de mayor calidad.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS \_ poliedro \_ rápido**
</dt> <dd>

Usa las aproximaciones para mejorar la velocidad de los gráficos a costa de que se agreguen más gráficos a la malla.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**\_Calidad de Poliedro de D3DXUVATLAS \_**
</dt> <dd>

Proporciona gráficos de mejor calidad, pero requiere más tiempo y memoria de lo rápido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




