---
description: Alterna el estado literal de un parámetro. Un parámetro literal tiene un valor que no cambia durante la vigencia de un efecto.
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: 'ID3DXEffectCompiler:: SetLiteral (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.SetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5a64426381876458b601b741050a01e5f35d084c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362470"
---
# <a name="id3dxeffectcompilersetliteral-method"></a>ID3DXEffectCompiler:: SetLiteral (método)

Alterna el estado literal de un parámetro. Un parámetro literal tiene un valor que no cambia durante la vigencia de un efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de un parámetro. Vea [identificadores (Direct3D 9)](handles.md).

</dd> <dt>

*Literal* \[ de de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Establézcalo en **true** para que el parámetro sea un literal y **false** si el parámetro puede cambiar el valor durante la vigencia del sombreador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este método solo cambia si el parámetro es un literal o no. Para cambiar el valor de un parámetro, use un método como [**ID3DXBaseEffect:: SetBool**](id3dxbaseeffect--setbool.md) o [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).

Se debe llamar a esta función antes de que se compile el efecto. Este es un ejemplo de cómo puede usarse esta función:


```
    LPD3DXEFFECTCOMPILER pEffectCompiler;
    char errors[1000];
    HRESULT hr;
    
    hr = D3DXCreateEffectCompilerFromFile("shader.fx",
                                          NULL, NULL, 0,
                                          &pEffectCompiler, 
                                          &errors);
    
    //In the fx file, literalInt is declared as an int.
    //By calling this function, the compiler will treat
    //it as a literal (i.e. #define)
    hr = pEffectCompiler->SetLiteral("literalInt", TRUE);
    
    //create ten different variations of the same effect
    LPD3DXBUFFER pEffects[10];
    LPD3DXBUFFER pErrors;
    for(int i = 0; i < 10; ++i)
    {
        hr = pEffectCompiler->SetInt("literalInt", i);
    
        hr = pEffectCompiler->CompileEffect(0, &pEffects[i], &pErrors);
    }
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Usos y literales (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler::GetLiteral**](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
