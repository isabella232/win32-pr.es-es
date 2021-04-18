---
description: Dibuja un subconjunto de una malla.
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: ID3DXBaseMesh::D método rawSubset (D3DX9Mesh. h)
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
ms.openlocfilehash: d0da6e9fc57e0fc5e7b4b263ba3d97185333881c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707851"
---
# <a name="id3dxbasemeshdrawsubset-method"></a>ID3DXBaseMesh::D método rawSubset

Dibuja un subconjunto de una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AttribId* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

DWORD que especifica el subconjunto de la malla que se va a dibujar. Este valor se usa para diferenciar caras en una malla como perteneciente a uno o varios grupos de atributos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

El subconjunto especificado por AttribId se representará mediante el método [**rawindexedprimitive de IDirect3DDevice9::D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) , mediante el \_ tipo primitivo D3DPT TRIANGLELIST, por lo que un búfer de índice debe estar inicializado correctamente.

Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con distintas texturas, Estados de representación, materiales, etc. Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla sin dibujar un identificador de atributo determinado (*AttribId*) al dibujar el marco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
