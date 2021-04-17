---
description: Convierte el subconjunto de malla especificado en una franja de triángulo única.
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: Función D3DXConvertMeshSubsetToSingleStrip (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToSingleStrip
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c76aa52b08a21faf9bc2a6ef35745513063cc3b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670219"
---
# <a name="d3dxconvertmeshsubsettosinglestrip-function"></a>D3DXConvertMeshSubsetToSingleStrip función)

Convierte el subconjunto de malla especificado en una franja de triángulo única.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXConvertMeshSubsetToSingleStrip(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Malla* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntero a una interfaz [**ID3DXBaseMesh**](id3dxbasemesh.md) que representa la malla que se va a convertir en una franja.

</dd> <dt>

*AttribId* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

IDENTIFICADOR de atributo del subconjunto de la malla que se va a convertir en franjas.

</dd> <dt>

*IBOptions* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas de la enumeración [**D3DXMESH**](./d3dxmesh.md) , especificando las opciones para crear el búfer de índice. No se puede D3DXMESH \_ 32 bits. El búfer de índice se creará con índices de 32 bits o de 16 bits, en función del formato del búfer de índice de la malla especificada por el parámetro *meshen* .

</dd> <dt>

*ppIndexBuffer* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

Puntero a una interfaz [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) que representa el búfer de índice que contiene la franja.

</dd> <dt>

*pNumIndices* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Número de índices en el búfer devuelto en el parámetro *ppIndexBuffer* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Antes de ejecutar esta función, llame a [**Optimize**](id3dxmesh--optimize.md) o [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)con el \_ indicador D3DXMESHOPT ATTRSORT establecido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
