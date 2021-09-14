---
description: Obtiene un estado literal de un parámetro. Un parámetro literal tiene un valor que no cambia durante la vigencia de un efecto.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: Método ID3DXEffectCompiler::GetLiteral (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c16e3798ab66a34e12812a3560572c45b9206b30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964764"
---
# <a name="id3dxeffectcompilergetliteral-method"></a>Método ID3DXEffectCompiler::GetLiteral

Obtiene un estado literal de un parámetro. Un parámetro literal tiene un valor que no cambia durante la vigencia de un efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de un parámetro. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pLiteral* \[ out\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)\***

Devuelve True si el parámetro es un literal y False en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este método solo cambia si el parámetro es un literal o no. Para cambiar el valor de un parámetro, use un método como [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) o [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Usos y literales (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler::SetLiteral**](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
