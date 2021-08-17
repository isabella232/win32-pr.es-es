---
description: Cambia el número de muestras contenidas en el búfer.
ms.assetid: c3cceba8-0bbc-46e5-95d9-cdf58d8a2510
title: Método ID3DXPRTBuffer::Resize (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.Resize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c6da4c5de4b38f5fe86b36622b7032e10ffe1be794ee8990ba19362cfd77d98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730078"
---
# <a name="id3dxprtbufferresize-method"></a>Método ID3DXPRTBuffer::Resize

Cambia el número de muestras contenidas en el búfer.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Resize(
  [in] UINT NewSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewSize* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de muestras que se incluirán en el búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, se devolverá el siguiente valor, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
