---
description: Obtiene el número de vértices en la malla.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'ID3DX10Mesh:: GetVertexCount (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 189be6ff6872cfb85c2f336c29dedef2e435382e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707985"
---
# <a name="id3dx10meshgetvertexcount-method"></a>ID3DX10Mesh:: GetVertexCount (método)

Obtiene el número de vértices en la malla. Una malla puede contener varios búferes de vértices (es decir, un búfer de vértices puede contener todos los datos de posición, otro puede contener todos los datos de coordenadas de textura, etc.); sin embargo, cada búfer de vértice contendrá el mismo número de elementos.

## <a name="syntax"></a>Sintaxis


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

El número de vértices en la malla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
