---
description: Establece un valor albedo para cada texel, sobrescribiendo los valores anteriores de albedo.
ms.assetid: 2928c861-a07e-4099-b04f-cdfa41e70874
title: Método ID3DXPRTEngine::SetPerTexelAlbedo (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6f17e4d3d3922c8e9d54b880f969c14b781935da34eab29b4ec1eb5d4d5421c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985555"
---
# <a name="id3dxprtenginesetpertexelalbedo-method"></a>Método ID3DXPRTEngine::SetPerTexelAlbedo

Establece un valor albedo para cada texel, sobrescribiendo los valores anteriores de albedo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPerTexelAlbedo(
  [in] LPDIRECT3DTEXTURE9        pAlbedoTexture,
  [in] UINT                      NumChannels,
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAlbedoTexture* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a un [**objeto de textura IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) en el que se almacenarán los valores de albedo.

</dd> <dt>

*NumChannels* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de canales de color que se establecerán. Establezca en 1 para especificar materiales grises (R = G = B) o 3 para habilitar los efectos de color.

</dd> <dt>

*pGH* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Puntero opcional a un [**objeto ID3DXTextureGutterHelper.**](id3dxtexturegutterhelper.md) Si no se proporciona, se crea y destruye internamente un objeto auxiliar de canales de textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLED3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ WASSTPLANTDRAWING, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
