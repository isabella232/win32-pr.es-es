---
description: Obtiene los nombres del muestreador a los que se hace referencia en un sombreador.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: Función D3DXGetShaderSamplers (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568421"
---
# <a name="d3dxgetshadersamplers-function"></a>Función D3DXGetShaderSamplers

Obtiene los nombres del muestreador a los que se hace referencia en un sombreador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFunction* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a la secuencia DWORD de la función de sombreador.

</dd> <dt>

*pSamplers* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Puntero a una matriz de LPCSTRs. La función rellenará esta matriz con punteros a los nombres de muestreador incluidos en *pFunction*. El tamaño máximo de la matriz es el número máximo de registros de muestreador (16 para vs \_ 3 \_ 0 y ps \_ 3 \_ 0).

Para buscar el número de muestreadores usados, compruebe *pCount* después de llamar a **D3DXGetShaderSamplers** con pSamplers = **NULL.**

</dd> <dt>

*pCount* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Devuelve el número de muestreadores a los que hace referencia el sombreador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
