---
description: Toma una malla y devuelve una nueva malla con pesos de mezcla por vértice y una tabla de combinación de hueso. En la tabla se describen los huesos que afectan a los subconjuntos de la malla.
ms.assetid: c26a9e84-5731-4394-a047-5f1ffe7688d9
title: 'ID3DXSkinInfo:: ConvertToBlendedMesh (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 051c51291416dd7e190c83433a9bf84baeb92957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718478"
---
# <a name="id3dxskininfoconverttoblendedmesh-method"></a>ID3DXSkinInfo:: ConvertToBlendedMesh (método)

Toma una malla y devuelve una nueva malla con pesos de mezcla por vértice y una tabla de combinación de hueso. En la tabla se describen los huesos que afectan a los subconjuntos de la malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConvertToBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Malla de entrada. Vea [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*Opciones* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Actualmente no se usa.

</dd> <dt>

*pAdjacencyIn* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Información de proximidad de la malla de entrada.

</dd> <dt>

*pAdjacencyOut* \[ de\]
</dt> <dd>

Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Información de proximidad de la malla de salida.

</dd> <dt>

*pFaceRemap* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matriz de DWORDs, una por cada tipo, que identifica la superficie de la malla original que corresponde a cada una de las caras de la malla combinada. Si el valor proporcionado para este argumento es **null**, no se devuelven los datos de reasignación de caras.

</dd> <dt>

*ppVertexRemap* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) , que contiene un valor DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices anteriores. Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices. Este parámetro es opcional; Se puede utilizar **null** .

</dd> <dt>

*pMaxVertexInfl* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a un valor DWORD que contendrá el número máximo de influencias del hueso necesarias por vértice para este método de la piel.

</dd> <dt>

*pNumBoneCombinations* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al número de huesos en la tabla de combinación de hueso.

</dd> <dt>

*ppBoneCombinationTable* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a la tabla de combinación de hueso. Los datos se organizan en una estructura [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .

</dd> <dt>

*ppMesh* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntero a la nueva malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Cada elemento de la matriz de reasignación especifica el índice anterior para esa posición. Por ejemplo, si un vértice estaba en la posición 3 pero se ha reasignado a la posición 5, el quinto elemento de pVertexRemap contendrá 3.

Este método no se ejecuta en hardware que no admite la combinación de vértices de funciones fijas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
