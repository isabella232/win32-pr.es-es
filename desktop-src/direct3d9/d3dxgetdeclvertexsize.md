---
description: Devuelve el tamaño de un vértice de la declaración de vértice.
ms.assetid: a2524f96-103e-43ab-bdcb-b99e7402fd89
title: Función D3DXGetDeclVertexSize (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c962064faa61dc7045b0111c5efbf1d1bea9fd40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567904"
---
# <a name="d3dxgetdeclvertexsize-function"></a>Función D3DXGetDeclVertexSize

Devuelve el tamaño de un vértice de la declaración de vértice.

## <a name="syntax"></a>Sintaxis


```C++
UINT D3DXGetDeclVertexSize(
  _In_ const D3DVERTEXELEMENT9 *pDecl,
  _In_       DWORD             Stream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDecl* \[ En\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Puntero a la declaración de vértice. Vea [**D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

</dd> <dt>

*Stream* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de flujo de base cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Tamaño de declaración de vértice, en bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
