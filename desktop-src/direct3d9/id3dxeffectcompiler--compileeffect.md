---
description: Compile un efecto.
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: Método ID3DXEffectCompiler::CompileEffect (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f3769f3f7433aadc55e766d68ecc152a4e26444cf506344f80e3f11a0bca8fcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951665"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a>Método ID3DXEffectCompiler::CompileEffect

Compile un efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de compilación identificadas por varias marcas. El compilador HLSL de Direct3D 10 es ahora el valor predeterminado. Consulte [D3DXSHADER Flags (Marcas de D3DXSHADER)](d3dxshader-flags.md) para obtener más información.

</dd> <dt>

*ppEffect* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Búfer que contiene el efecto compilado. Para obtener más información sobre el acceso al búfer, [**vea ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppErrorMsgs* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Búfer que contiene al menos el primer mensaje de error de compilación que se produjo. Esto incluye los errores del compilador de efecto y los errores de compilación de lenguaje de alto nivel. Para obtener más información sobre el acceso al búfer, [**vea ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK.

Si los argumentos no son válidos, el método devolverá D3DERR \_ INVALIDCALL.

Si se produce un error en el método, el valor devuelto será E \_ FAIL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> </dl>

 

 
