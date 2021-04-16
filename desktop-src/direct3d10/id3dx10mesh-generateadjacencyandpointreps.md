---
description: Generar una lista de bordes de la malla, así como una lista de caras que comparten cada borde.
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'ID3DX10Mesh:: GenerateAdjacencyAndPointReps (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c46cf83931c95116132798ca971f9d4e61da2af8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548014"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a>ID3DX10Mesh:: GenerateAdjacencyAndPointReps (método)

Generar una lista de bordes de la malla, así como una lista de caras que comparten cada borde.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Épsilon* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Especifica que los vértices que difieren en la posición inferior al épsilon se deben tratar como coincidentes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Una vez que una aplicación genera información de adyacencias para una malla, los datos de la malla pueden optimizarse para mejorar el rendimiento del dibujo.

El orden de las entradas en el búfer de adyacencia viene determinado por el orden de los índices de vértice en el búfer de índice. El triángulo 0 adyacente siempre corresponde al borde entre los índices de las esquinas 0 y 1. El triángulo 1 adyacente siempre corresponde al borde entre los índices de las esquinas 1 y 2, mientras que el triángulo 2 adyacente se corresponde con el borde entre los índices de las esquinas 2 y 0.

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

 

 
