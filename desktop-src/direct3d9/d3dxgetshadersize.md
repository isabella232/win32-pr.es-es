---
description: Devuelve el tamaño del código de byte del sombreador, en bytes.
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: Función D3DXGetShaderSize (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3017c5a5371e99bcf9e1d69827de0227d929f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717756"
---
# <a name="d3dxgetshadersize-function"></a>D3DXGetShaderSize función)

Devuelve el tamaño del código de byte del sombreador, en bytes.

## <a name="syntax"></a>Sintaxis


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFunction* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a la secuencia DWORD de la función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Devuelve el tamaño del código de byte del sombreador, en bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones del sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
