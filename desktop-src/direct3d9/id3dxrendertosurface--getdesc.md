---
description: Recupera los parámetros de la superficie de representación.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'ID3DXRenderToSurface:: GetDesc (método) (D3dx9core. h)'
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
ms.openlocfilehash: 00824c6b418a3e6707ebfd588d8d32d4e38f173d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280494"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a>ID3DXRenderToSurface:: GetDesc (método)

Recupera los parámetros de la superficie de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pParameters* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXRTS \_ DESC**](d3dxrts-desc.md)\***

Puntero a una [**estructura \_ DESC de D3DXRTS**](d3dxrts-desc.md) , que describe los parámetros de la superficie de representación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 




