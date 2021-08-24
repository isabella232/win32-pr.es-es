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
ms.openlocfilehash: 55198648be8952f975313dad3019063917eddf4d38f0a7d636039d5802f08e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566945"
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

El orden de las entradas del búfer de adyacencia viene determinado por el orden de los índices de vértices en el búfer de índice. El triángulo adyacente 0 siempre se corresponde con el borde entre los índices de las esquinas 0 y 1. El triángulo adyacente 1 siempre se corresponde con el borde entre los índices de las esquinas 1 y 2, mientras que el triángulo adyacente 2 corresponde al borde entre los índices de las esquinas 2 y 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
