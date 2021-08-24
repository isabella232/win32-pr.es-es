---
description: Recupera los parámetros de la superficie de representación.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: Método ID3DXRenderToSurface::GetDesc (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7dd6787ad8a81491e92af2a5ec1a16253af4cd0a0f8cb075dde01461b0010d45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790485"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a>Método ID3DXRenderToSurface::GetDesc

Recupera los parámetros de la superficie de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pParameters* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXRTS \_ DESC**](d3dxrts-desc.md)\***

Puntero a una [**estructura D3DXRTS \_ DESC,**](d3dxrts-desc.md) que describe los parámetros de la superficie de representación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 




