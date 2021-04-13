---
description: Obtiene un puntero a la tabla de constantes.
ms.assetid: 5d836d99-783f-41e1-b7bf-d874d09a4892
title: 'ID3DXTextureShader:: GetConstantBuffer (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c83a723dde56fc80f643d7209c56fc05ad6cce5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362499"
---
# <a name="id3dxtextureshadergetconstantbuffer-method"></a>ID3DXTextureShader:: GetConstantBuffer (método)

Obtiene un puntero a la tabla de constantes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConstantBuffer(
  [out] LPD3DXBUFFER *ppConstantBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppConstantBuffer* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) , que contiene las constantes.

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

 

 




