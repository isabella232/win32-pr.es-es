---
description: Obtiene un valor de punto flotante.
ms.assetid: 239dd29c-092a-4b9f-ba24-eb6181e91461
title: Método ID3DXBaseEffect::GetFloat (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 51edaa1872223727abdc396766552720cd34d726
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888508"
---
# <a name="id3dxbaseeffectgetfloat-method"></a>Método ID3DXBaseEffect::GetFloat

Obtiene un valor de punto flotante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFloat(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pf* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Devuelve un valor de punto flotante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetFloat**](id3dxbaseeffect--setfloat.md)
</dt> </dl>

 

 
