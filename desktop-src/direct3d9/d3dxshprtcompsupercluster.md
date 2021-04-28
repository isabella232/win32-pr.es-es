---
description: 'Función D3DXSHPRTCompSuperCluster: se usa con los resultados comprimidos de la versión de vértice del simulador de transferencia de radiancia (PRT) precalutado.'
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: Función D3DXSHPRTCompSuperCluster (D3DX9Mesh.h)
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
ms.openlocfilehash: 0c22c8a3a14fd8af3e9104889b421068c7ff1457
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117863"
---
# <a name="d3dxshprtcompsupercluster-function"></a>Función D3DXSHPRTCompSuperCluster

Se usa con resultados comprimidos de la versión de vértice del simulador de transferencia de radiancia precalutada (PRT). Genera "superclústeres", que son grupos de clústeres que se pueden dibujar en la misma llamada a draw. Se usa un algoritmo expansión que minimiza el sobredesgráfico para agrupar los clústeres.

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

*pClusterIDs* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero a los IDs de clúster numverts (extraídos de un búfer comprimido).

</dd> <dt>

*pScene* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una malla que representa la escena compuesta pasada al simulador. Vea [**ID3DXMesh.**](id3dxmesh.md)

</dd> <dt>

*MaxNumClusters* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número máximo de clústeres asignados por super clúster.

</dd> <dt>

*NumClusters* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de clústeres calculados en el simulador.

</dd> <dt>

*pSClusterIDs* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero a una matriz de *longitud NumClusters.* Contiene el índice del superc cluster al que se asignó el clúster correspondiente.

</dd> <dt>

*pNumSCs* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Número de super clústeres asignados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de transferencia de radiancia precalcaladas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
