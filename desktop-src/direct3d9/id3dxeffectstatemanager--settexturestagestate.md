---
description: Función de devolución de llamada que debe implementar un usuario para establecer el estado de la fase de textura.
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: Método ID3DXEffectStateManager::SetTextureStageState (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTextureStageState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5a74642d97532020679749d54924f4ab4052100d638d2bbd902b7b721fc75610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520990"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a>Método ID3DXEffectStateManager::SetTextureStageState

Función de devolución de llamada que debe implementar un usuario para establecer el estado de la fase de textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTextureStageState(
  [in] DWORD                    Stage,
  [in] D3DTEXTURESTAGESTATETYPE Type,
  [in] DWORD                    Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Fase* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Fase a la que se asigna la textura. Este es el valor de índice de [**IDirect3DDevice9::SetTexture**](/windows/desktop/api) o [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).

</dd> <dt>

*Tipo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**

Define el tipo de operación que realizará una fase de textura. Vea [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).

</dd> <dt>

*Valor* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Puede ser una operación ([**D3DTEXTUREOP**](./d3dtextureop.md)) o un valor de argumento ([D3DTA](d3dta.md)), en función de lo que se elija para Tipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ OK. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9::SetTextureStageState).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
