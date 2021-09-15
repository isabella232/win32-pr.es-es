---
description: Obtiene la semántica de las entradas del sombreador. Use este método para determinar el formato de vértice de entrada.
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: Función D3DXGetShaderInputSemantics (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567872"
---
# <a name="d3dxgetshaderinputsemantics-function"></a>Función D3DXGetShaderInputSemantics

Obtiene la semántica de las entradas del sombreador. Use este método para determinar el formato de vértice de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXGetShaderInputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFunction* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a la secuencia DWORD de la función de sombreador.

</dd> <dt>

*pSemantics* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***

Puntero a una matriz de [**estructuras D3DXSEMANTIC.**](d3dxsemantic.md) La función rellenará esta matriz con la semántica de cada elemento de entrada al que hace referencia el sombreador. Se supone que esta matriz contiene al menos elementos MAXD3DDECLLENGTH. Sin embargo, al llamar a **D3DXGetShaderInputSemantics** con pSemantics = **NULL,** se devolverá el número de elementos necesarios para pCount.

</dd> <dt>

*pCount* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Devuelve el número de elementos de pSemantics.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Use **D3DXGetShaderInputSemantics** para devolver una lista de la semántica de entrada requerida por el sombreador. Esta es la manera de averiguar cuál es el formato de vértice de entrada para un sombreador de lenguaje de sombreador de alto nivel (HLSL). Si el sombreador tiene entradas adicionales que faltan en la declaración de vértice, podría crear un flujo de vértice adicional que tenga un paso de 0 que tenga los componentes que faltan con los valores predeterminados. Por ejemplo, esta técnica podría usarse para proporcionar el color de vértice predeterminado para los modelos que no lo especifican.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
