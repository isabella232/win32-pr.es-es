---
description: 'Método ID3DXBaseMesh::D rawSubset: dibuja un subconjunto de una malla.'
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: Método ID3DXBaseMesh::D rawSubset (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.DrawSubset
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 252c9b9921c7eafd8f0c2a54cfa14a85e91b8f7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115473"
---
# <a name="id3dxbasemeshdrawsubset-method"></a>Método ID3DXBaseMesh::D rawSubset

Dibuja un subconjunto de una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AttribId* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

DWORD que especifica qué subconjunto de la malla se va a dibujar. Este valor se usa para diferenciar las caras de una malla como pertenecientes a uno o varios grupos de atributos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

El subconjunto especificado por AttribId se representará mediante el método [**IDirect3DDevice9::D rawIndexedPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) mediante el tipo primitivo D3DPT TRIANGLELIST, por lo que se debe inicializar correctamente un búfer de \_ índice.

Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otras. Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla no dibujando un identificador de atributo determinado (*AttribId*) al dibujar el marco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
