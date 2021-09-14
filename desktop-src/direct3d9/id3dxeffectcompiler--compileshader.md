---
description: Compila un sombreador a partir de un efecto que contiene una o varias funciones.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: Método ID3DXEffectCompiler::CompileShader (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3e8d1d72fccd5c4ad47d21d05ee46013860a7743
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964767"
---
# <a name="id3dxeffectcompilercompileshader-method"></a>Método ID3DXEffectCompiler::CompileShader

Compila un sombreador a partir de un efecto que contiene una o varias funciones.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFunction* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de la función que se va a compilar. Este valor no debe ser **NULL.** Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pTarget* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a un perfil de sombreador que determina el conjunto de instrucciones del sombreador. Consulte [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para obtener una lista de los perfiles disponibles.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de compilación identificadas por varias marcas. El compilador HLSL de Direct3D 10 es ahora el valor predeterminado. Consulte [D3DXSHADER Flags (Marcas de D3DXSHADER)](d3dxshader-flags.md) para obtener más información.

</dd> <dt>

*ppShader* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Búfer que contiene el sombreador compilado. El sombreador del compilador es una matriz de DWORD. Para obtener más información sobre el acceso al búfer, [**vea ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppErrorMsgs* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Búfer que contiene al menos el primer mensaje de error de compilación que se produjo. Esto incluye los errores del compilador de efecto y los errores de compilación de lenguaje de alto nivel. Para obtener más información sobre el acceso al búfer, [**vea ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppConstantTable* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Devuelve una [**interfaz ID3DXConstantTable,**](id3dxconstanttable.md) que se puede usar para tener acceso a las constantes del sombreador. Este valor puede ser **NULL.** Si compila la aplicación como una dirección grande (es decir, usa la opción del vinculador /LARGEADDRESSAWARE para controlar direcciones de más de 2 GB), no puede usar este parámetro y debe establecerlo en **NULL.** En su lugar, debe usar la función [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar la tabla shader-constant incrustada dentro del sombreador. En esta **llamada a D3DXGetShaderConstantTableEx,** debe pasar la marca **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parámetro *Flags* para especificar el acceso a hasta 4 GB de espacio de direcciones virtuales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK.

Si los argumentos no son válidos, el método devolverá D3DERR \_ INVALIDCALL.

Si se produce un error en el método , el valor devuelto será E \_ FAIL.

## <a name="remarks"></a>Observaciones

Los destinos se pueden especificar para sombreadores de vértices, sombreadores de píxeles y funciones de relleno de textura.



| Destinos                      | Functions                                                                      |
|-----------------------|-----------------------------------------------------------------------|
| Destinos del sombreador de vértices | vs \_ 1 \_ 1, vs \_ 2 \_ 0, vs \_ 2 \_ sw, vs \_ 3 \_ 0                               |
| Destinos del sombreador de píxeles  | ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4, ps \_ 2 \_ 0, ps \_ 2 \_ sw, ps \_ 3 \_ 0 |
| Destinos de relleno de textura  | tx \_ 0, tx \_ 1                                                          |



 

Este método compila un sombreador a partir de una función escrita en un lenguaje de tipo C. Para obtener más información, vea [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
