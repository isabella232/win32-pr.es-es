---
description: Se usa con los resultados comprimidos de la versión de vértice del simulador Radiance Transfer (PRT) precalculado.
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: Función D3DXSHPRTCompSuperCluster (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1daf25dddfaf738ecc2fed9605429a19170177ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362541"
---
# <a name="d3dxshprtcompsupercluster-function"></a>D3DXSHPRTCompSuperCluster función)

Se usa con los resultados comprimidos de la versión de vértice del simulador Radiance Transfer (PRT) precalculado. Genera "superclústeres", que son grupos de clústeres que se pueden dibujar en la misma llamada a Draw. Se usa un algoritmo expansivo que minimiza el desdibujo para agrupar los clústeres.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pClusterIDs* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntero a los identificadores de clúster de NumVerts (extraídos de un búfer comprimido).

</dd> <dt>

*pScene* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una malla que representa la escena compuesta pasada al simulador. Vea [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*MaxNumClusters* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de clústeres asignados por Super cluster.

</dd> <dt>

*NumClusters* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de clústeres calculados en el simulador.

</dd> <dt>

*pSClusterIDs* \[ in, out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntero a una matriz de longitud *NumClusters*. Contiene el índice del clúster Super al que se asignó el clúster correspondiente.

</dd> <dt>

*pNumSCs* \[ in, out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Número de clústeres superpuestos asignados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de transferencia Radiance precalculadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
