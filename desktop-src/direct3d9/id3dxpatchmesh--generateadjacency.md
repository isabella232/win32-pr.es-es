---
description: Genere una lista de bordes de malla y las revisiones que comparten cada borde.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: Método ID3DXPatchMesh::GenerateAdjacency (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68de2a77b9d27391c57ec299ceb87d29166ee248
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060556"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a>Método ID3DXPatchMesh::GenerateAdjacency

Genere una lista de bordes de malla y las revisiones que comparten cada borde.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fTolerance* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Especifica que los vértices que difieren en posición en menor que la tolerancia deben tratarse como coincidentes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Una vez que una aplicación genera información de adyacencia para una malla, los datos de la malla se pueden optimizar para mejorar el rendimiento del dibujo. Este método determina qué revisiones son adyacentes (dentro de la tolerancia proporcionada). Esta información se usa internamente para optimizar la teselación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
