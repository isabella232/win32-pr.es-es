---
description: La interfaz ID3DXEffectCompiler compila un efecto de una función o de un sombreador de vértices.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: Interfaz ID3DXEffectCompiler (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c7a16417528d1adbd9ba54f9bd7120057654d14e0ef4bddad829e8f232445069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856745"
---
# <a name="id3dxeffectcompiler-interface"></a>Interfaz ID3DXEffectCompiler

La **interfaz ID3DXEffectCompiler** compila un efecto de una función o de un sombreador de vértices.

## <a name="members"></a>Miembros

La **interfaz ID3DXEffectCompiler** hereda de [**ID3DXBaseEffect**](id3dxbaseeffect.md). **ID3DXEffectCompiler** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXEffectCompiler** tiene estos métodos.



| Método                                                      | Descripción                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) | Compile un efecto.<br/>                                                                                                               |
| [**CompileShader**](id3dxeffectcompiler--compileshader.md) | Compila un sombreador a partir de un efecto que contiene una o varias funciones.<br/>                                                            |
| [**GetLiteral**](id3dxeffectcompiler--getliteral.md)       | Obtiene un estado literal de un parámetro. Un parámetro literal tiene un valor que no cambia durante la vigencia de un efecto.<br/>      |
| [**SetLiteral**](id3dxeffectcompiler--setliteral.md)       | Alterna el estado literal de un parámetro. Un parámetro literal tiene un valor que no cambia durante la vigencia de un efecto.<br/> |



 

## <a name="remarks"></a>Comentarios

La interfaz ID3DXEffectCompiler se obtiene llamando a [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)o [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).

El tipo LPD3DXEFFECTCOMPILER se define como un puntero a esta interfaz.


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Interfaces de efecto](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 




