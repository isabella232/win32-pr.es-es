---
description: 'Método ID3DXBaseEffect::SetBool: establece un valor BOOL.'
ms.assetid: bb7c4860-50a0-416a-b9e0-5a2bec113e3c
title: Método ID3DXBaseEffect::SetBool (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5045c26f521da289899c8f8bc0d97b7eaf01826f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569920"
---
# <a name="id3dxbaseeffectsetbool-method"></a>Método ID3DXBaseEffect::SetBool

Establece un valor BOOL.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       b
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*b* \[ en\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Valor booleano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetBool**](id3dxbaseeffect--getbool.md)
</dt> </dl>

 

 
