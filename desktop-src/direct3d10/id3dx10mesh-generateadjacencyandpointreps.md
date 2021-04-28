---
description: 'Método ID3DX10Mesh::GenerateAdjacencyAndPointReps: genera una lista de bordes de malla, así como una lista de caras que comparten cada borde.'
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: Método ID3DX10Mesh::GenerateAdjacencyAndPointReps (D3DX10.h)
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
ms.openlocfilehash: e496f96f36805d411c71e9aba1e2560b0dcbe3c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083983"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a>Método ID3DX10Mesh::GenerateAdjacencyAndPointReps

Genere una lista de bordes de malla, así como una lista de caras que comparten cada borde.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Epsilon* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Especifica que los vértices que difieren en posición por menos de epsilon deben tratarse como coincidentes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Una vez que una aplicación genera información de adyacencia para una malla, los datos de la malla se pueden optimizar para mejorar el rendimiento del dibujo.

El orden de las entradas del búfer de adyacencia viene determinado por el orden de los índices de vértices en el búfer de índice. El triángulo adyacente 0 siempre se corresponde con el borde entre los índices de las esquinas 0 y 1. El triángulo adyacente 1 siempre se corresponde con el borde entre los índices de las esquinas 1 y 2, mientras que el triángulo adyacente 2 se corresponde con el borde entre los índices de las esquinas 2 y 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
