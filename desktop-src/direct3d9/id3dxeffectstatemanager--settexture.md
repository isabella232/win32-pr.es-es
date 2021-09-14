---
description: Función de devolución de llamada que debe implementar un usuario para establecer una textura.
ms.assetid: 971802f4-ea7a-4906-83b8-0cd83111716e
title: Método ID3DXEffectStateManager::SetTexture (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b395c19b65bb39b8328da24f727292f7dbe2a0f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060617"
---
# <a name="id3dxeffectstatemanagersettexture-method"></a>Método ID3DXEffectStateManager::SetTexture

Función de devolución de llamada que debe implementar un usuario para establecer una textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTexture(
  [in] DWORD                  Stage,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Fase* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Fase a la que se asigna la textura. Este es el valor de índice [**de IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) o [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).

</dd> <dt>

*pTexture* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Puntero al objeto de textura. Puede ser cualquiera de los tipos de textura de Direct3D (cubo, volumen, etc.). Vea [**IDirect3DBaseTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ OK. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (por [**ejemplo, IDirect3DDevice9::SetTexture).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
