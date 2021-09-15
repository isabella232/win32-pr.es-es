---
description: 'Función D3DXGetShaderConstantTableEx: obtiene la tabla shader-constant incrustada dentro de un sombreador.'
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: Función D3DXGetShaderConstantTableEx (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cac525f6f6fc4f4e3b6e5900aa9b655e7c7f60d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567877"
---
# <a name="d3dxgetshaderconstanttableex-function"></a>Función D3DXGetShaderConstantTableEx

Obtiene la tabla shader-constant incrustada dentro de un sombreador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFunction* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a la secuencia DWORD de la función.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Use la marca LARGEADDRESSAWARE de D3DXCONSTTABLE para acceder a hasta 4 GB de espacio de direcciones virtuales (en lugar del valor predeterminado \_ de 2 GB). Si no necesita el espacio de direcciones virtuales adicional, use [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).

</dd> <dt>

 *ppConstantTable* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Devuelve la interfaz de tabla constante [**(vea ID3DXConstantTable)**](id3dxconstanttable.md)que administra la tabla constante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

[**D3DXCompileShader**](d3dxcompileshader.md) genera una tabla constante e incrustada en el cuerpo del sombreador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
