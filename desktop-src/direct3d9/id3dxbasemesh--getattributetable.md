---
description: 'Método ID3DXBaseMesh::GetAttributeTable: recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.'
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: Método ID3DXBaseMesh::GetAttributeTable (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f5d27de884f72b46db900487e26f1099bf30949
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115453"
---
# <a name="id3dxbasemeshgetattributetable-method"></a>Método ID3DXBaseMesh::GetAttributeTable

Recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAttribTable* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***

Puntero a una matriz de [**estructuras D3DXATTRIBUTERANGE,**](d3dxattributerange.md) que representan las entradas de la tabla de atributos de la malla. Especifique **NULL** para recuperar el valor de pAttribTableSize.

</dd> <dt>

*pAttribTableSize* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al número de entradas almacenadas en pAttribTable o a un valor que se va a rellenar con el número de entradas almacenadas en la tabla de atributos de la malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

[**Id3DXMesh::Optimize**](id3dxmesh--optimize.md) crea una tabla de atributos y pasa D3DXMESHOPT \_ ATTRSORT para el parámetro Flags.

Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otras. Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla al no dibujar un identificador de atributo determinado al dibujar el marco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
