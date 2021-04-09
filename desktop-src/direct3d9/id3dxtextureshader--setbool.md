---
description: Establece un valor BOOLEANO.
ms.assetid: 0d3c1f3a-f497-4e92-81e9-8647006910e1
title: 'ID3DXTextureShader:: SetBool (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49fbc2d2841957e75a8bc3adaf40ce0fdf5e2a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821359"
---
# <a name="id3dxtextureshadersetbool-method"></a>ID3DXTextureShader:: SetBool (método)

Establece un valor BOOLEANO.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hConstant,
  [in] BOOL       b
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de la constante. Vea [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*b* \[ en\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Valor BOOLEANO.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
