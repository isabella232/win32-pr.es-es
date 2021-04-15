---
description: Comienza una escena.
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: 'ID3DXRenderToSurface:: BeginScene (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.BeginScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5aa2229e88123cc1d52f65f1edf032c46f819229
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649451"
---
# <a name="id3dxrendertosurfacebeginscene-method"></a>ID3DXRenderToSurface:: BeginScene (método)

Comienza una escena.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSurface* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Puntero a una interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) que representa la superficie de representación.

</dd> <dt>

*pViewport* \[ de\]
</dt> <dd>

Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Puntero a una estructura [**D3DVIEWPORT9**](d3dviewport9.md) , que describe la ventanilla de la escena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL. D3DERR \_ OUTOFVIDEOMEMORY D3DXERR \_ INVALIDDATA E \_ OUTOFMEMORY

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> <dt>

[**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 
