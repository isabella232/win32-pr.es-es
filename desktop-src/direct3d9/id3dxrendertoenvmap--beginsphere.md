---
description: Inicie la representación de un mapa de entorno esférico.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'ID3DXRenderToEnvMap:: BeginSphere (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 872aa06734ae818ef248b03fbc14dcd1c33fe815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362513"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a>ID3DXRenderToEnvMap:: BeginSphere (método)

Inicie la representación de un mapa de entorno esférico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTex* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura a la que se va a representar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL. E \_ FAIL

## <a name="remarks"></a>Observaciones

Vea [**ID3DXRenderToEnvMap:: facial**](id3dxrendertoenvmap--face.md) para dibujar la superficie.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap:: end**](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
