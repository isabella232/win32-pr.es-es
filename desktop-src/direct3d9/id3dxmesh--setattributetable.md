---
description: 'Método ID3DXMesh::SetAttributeTable: establece la tabla de atributos para una malla y el número de entradas almacenadas en la tabla.'
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: Método ID3DXMesh::SetAttributeTable (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4cdb503e934ca00b41482601b59266eee750365
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093353"
---
# <a name="id3dxmeshsetattributetable-method"></a>Método ID3DXMesh::SetAttributeTable

Establece la tabla de atributos para una malla y el número de entradas almacenadas en la tabla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAttribTable* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***

Puntero a una matriz de [**estructuras D3DXATTRIBUTERANGE,**](d3dxattributerange.md) que representa las entradas de la tabla de atributos de malla.

</dd> <dt>

*cAttribTableSize* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de atributos de la tabla de atributos de malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Si una aplicación realiza un seguimiento de la información de una tabla de atributos y reorganiza la tabla como resultado de cambios en atributos o caras, este método permite a la aplicación actualizar las tablas de atributos en lugar de llamar de nuevo a [**ID3DXMesh::Optimize.**](id3dxmesh--optimize.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

**ID3DXMesh::LockAttributeBuffer**
</dt> </dl>

 

 
