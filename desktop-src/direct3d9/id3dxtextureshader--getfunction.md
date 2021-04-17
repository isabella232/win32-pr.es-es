---
description: Obtiene un puntero a la secuencia DWORD de la función.
ms.assetid: a051b51a-185c-4a9e-a8b9-4096615e2634
title: 'ID3DXTextureShader:: GetFunction ((método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetFunction
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80e504e65e4c8437247b2935794025e1b693433a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708029"
---
# <a name="id3dxtextureshadergetfunction-method"></a>ID3DXTextureShader:: GetFunction ((método)

Obtiene un puntero a la secuencia DWORD de la función.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFunction(
  [in] LPD3DXBUFFER *ppFunction
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppFunction* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a la secuencia DWORD de la función. Vea [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 




