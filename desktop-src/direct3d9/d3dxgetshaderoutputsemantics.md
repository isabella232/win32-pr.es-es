---
description: Obtiene la semántica de todos los elementos de salida del sombreador.
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: Función D3DXGetShaderOutputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 264db967d2959c2f6e5096e0362e9db576ba9f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547894"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a>D3DXGetShaderOutputSemantics función)

Obtiene la semántica de todos los elementos de salida del sombreador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFunction* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a la secuencia DWORD de la función de sombreador.

</dd> <dt>

*pSemantics* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***

Puntero a una matriz de estructuras [**D3DXSEMANTIC**](d3dxsemantic.md) . La función rellenará esta matriz con la semántica de cada elemento de salida al que hace referencia el sombreador. Se supone que esta matriz contiene al menos elementos MAXD3DDECLLENGTH. Sin embargo, si se llama a **D3DXGetShaderOutputSemantics** con PSemantics = **null** , se devolverá el número de elementos necesarios para pCount.

</dd> <dt>

*pCount* \[ enuncia\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Devuelve el número de elementos de pSemantics.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones del sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
