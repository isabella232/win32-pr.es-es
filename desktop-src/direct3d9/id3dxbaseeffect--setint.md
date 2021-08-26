---
description: Establece un entero.
ms.assetid: 1090d4a6-b4f5-4e15-a49f-e2724f1c3f95
title: Método ID3DXBaseEffect::SetInt (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetInt
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 436ae9015ebe7d6aba203d0c696bed29323275775e5e5705577341f8152f5c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848625"
---
# <a name="id3dxbaseeffectsetint-method"></a>Método ID3DXBaseEffect::SetInt

Establece un entero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hParameter,
  [in] INT        n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*n* \[ en\]
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Valor entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetInt**](id3dxbaseeffect--getint.md)
</dt> </dl>

 

 
