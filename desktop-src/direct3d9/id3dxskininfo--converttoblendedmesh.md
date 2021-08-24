---
description: Toma una malla y devuelve una nueva malla con pesos de mezcla por vértice y una tabla de combinación de teclas. En la tabla se describe qué elementos afectan a qué subconjuntos de la malla.
ms.assetid: c26a9e84-5731-4394-a047-5f1ffe7688d9
title: Método ID3DXSkinInfo::ConvertToBlendedMesh (D3DX9Mesh.h)
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
ms.openlocfilehash: 026808748f0d94a4b5282bfdad6590e3c030ddf6ce0009bec5e59852e9984163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747685"
---
# <a name="id3dxskininfoconverttoblendedmesh-method"></a>Método ID3DXSkinInfo::ConvertToBlendedMesh

Toma una malla y devuelve una nueva malla con pesos de mezcla por vértice y una tabla de combinación de teclas. En la tabla se describe qué elementos afectan a qué subconjuntos de la malla.

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

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Malla de entrada. Vea [**ID3DXMesh.**](id3dxmesh.md)

</dd> <dt>

*Opciones* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Actualmente no se usa.

</dd> <dt>

*pAdjacencyIn* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Información de adyacencia de malla de entrada.

</dd> <dt>

*pAdjacencyOut* \[ En\]
</dt> <dd>

Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Información de adyacencia de malla de salida.

</dd> <dt>

*pFaceRemap* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matriz de DWORD, una por cara, que identifica la cara de malla original que corresponde a cada cara de la malla mezclada. Si el valor proporcionado para este argumento es **NULL,** no se devuelven los datos de reasignación de caras.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una interfaz [**ID3DXBuffer,**](id3dxbuffer.md) que contiene un DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices antiguos. Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices. Este parámetro es opcional; Se puede usar **NULL.**

</dd> <dt>

*pMaxVertexInfl* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a un DWORD que contendrá el número máximo de influencias de la pera requeridas por vértice para este método de despejado.

</dd> <dt>

*pNumMbiCombinations* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al número de tordos de la tabla de combinación de teclas.

</dd> <dt>

*ppCombinationTable* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a la tabla de combinación de teclas. Los datos se organizan en una [**estructura D3DXCCICOMBINATION.**](d3dxbonecombination.md)

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntero a la nueva malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Cada elemento de la matriz de reasignación especifica el índice anterior para esa posición. Por ejemplo, si un vértice estaba en la posición 3 pero se ha reasignado a la posición 5, el quinto elemento de pVertexRemap contendrá 3.

Este método no se ejecuta en hardware que no admite la mezcla de vértices de función fija.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
