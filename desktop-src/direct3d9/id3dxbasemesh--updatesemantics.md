---
description: Este método permite al usuario cambiar la declaración de la malla sin cambiar el diseño de los datos del búfer de vértices. La llamada solo es válida si los formatos de declaración anterior y nuevo tienen el mismo tamaño de vértice.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'ID3DXBaseMesh:: UpdateSemantics (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083739"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a>ID3DXBaseMesh:: UpdateSemantics (método)

Este método permite al usuario cambiar la declaración de la malla sin cambiar el diseño de los datos del búfer de vértices. La llamada solo es válida si los formatos de declaración anterior y nuevo tienen el mismo tamaño de vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Declaración* \[ de in, out\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que describe el formato de vértice de los vértices de malla. El límite superior de esta matriz de declarador es el [**tamaño máximo de \_ FVF \_ decl \_**](./max-fvf-decl-size.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

[**ID3DXBaseMesh:: CloneMesh**](id3dxbasemesh--clonemesh.md) se usa para volver a formatear y cambiar el diseño de los datos de vértices. Por ejemplo, úselo para agregar espacio para las normales, coordenadas de textura, colores, pesos, etc., que no estaban presentes antes.

**ID3DXBaseMesh:: UpdateSemantics** es un método para actualizar la declaración de vértices con información semántica diferente, sin cambiar el diseño del búfer de vértices. Por ejemplo, úselo para cambiar la etiqueta de una coordenada de textura 3D como binormalización o tangente, o viceversa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXBaseMesh::CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
