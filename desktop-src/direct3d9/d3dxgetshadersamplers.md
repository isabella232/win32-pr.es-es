---
description: Obtiene los nombres de muestra a los que se hace referencia en un sombreador.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: Función D3DXGetShaderSamplers (D3DX9Shader. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717757"
---
# <a name="d3dxgetshadersamplers-function"></a>D3DXGetShaderSamplers función)

Obtiene los nombres de muestra a los que se hace referencia en un sombreador.

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

*pFunction* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a la secuencia DWORD de la función de sombreador.

</dd> <dt>

*pSamplers* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Puntero a una matriz de LPCSTRs. La función rellenará esta matriz con punteros a los nombres de muestra contenidos dentro de *pFunction*. El tamaño máximo de la matriz es el número máximo de registros de muestra (16 para vs \_ 3 \_ 0 y PS \_ 3 \_ 0).

Para buscar el número de muestras usadas, compruebe *pCount* después de llamar a **D3DXGetShaderSamplers** con pSamplers = **null**.

</dd> <dt>

*pCount* \[ enuncia\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Devuelve el número de muestras a las que hace referencia el sombreador.

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

 

 
