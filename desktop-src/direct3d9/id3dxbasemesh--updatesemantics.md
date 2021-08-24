---
description: Este método permite al usuario cambiar la declaración de malla sin cambiar el diseño de datos del búfer de vértices. La llamada solo es válida si los formatos de declaración antiguos y nuevos tienen el mismo tamaño de vértice.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: Método ID3DXBaseMesh::UpdateSemantics (D3DX9Mesh.h)
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
ms.openlocfilehash: 3a9a628c16e7f4a26db9953298be1adcba2cef364153d4bb2e6b29dbc4d9ef83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607325"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a>Método ID3DXBaseMesh::UpdateSemantics

Este método permite al usuario cambiar la declaración de malla sin cambiar el diseño de datos del búfer de vértices. La llamada solo es válida si los formatos de declaración antiguos y nuevos tienen el mismo tamaño de vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Declaración* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matriz de [**elementos D3DVERTEXELEMENT9,**](d3dvertexelement9.md) que describe el formato de vértice de los vértices de la malla. El límite superior de esta matriz declarator es [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

[**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) se usa para volver a formatear y cambiar el diseño de datos del vértice. Por ejemplo, úselo para agregar espacio para normales, coordenadas de textura, colores, pesos, etc. que no estaban presentes antes.

**ID3DXBaseMesh::UpdateSemantics** es un método para actualizar la declaración de vértices con información semántica diferente, sin cambiar el diseño del búfer de vértices. Por ejemplo, úsela para volver a etiquetar una coordenada de textura 3D como binormal o tangente, o viceversa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXBaseMesh::CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
