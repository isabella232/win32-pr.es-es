---
description: Función de devolución de llamada que debe implementar un usuario para establecer una luz.
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: Método ID3DXEffectStateManager::SetLight (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 83250450a0510949267ffd52f17e6e9013a646d40229efcf7d5bcc7a396e1b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372085"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a>Método ID3DXEffectStateManager::SetLight

Función de devolución de llamada que debe implementar un usuario para establecer una luz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de base cero de la luz. Este es el mismo índice de [**IDirect3DDevice9::SetLight.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)

</dd> <dt>

*pLight* \[ En\]
</dt> <dd>

Tipo: **const [**D3DLight9**](d3dlight9.md) \***

Objeto claro. Vea [**D3DLIGHT9.**](d3dlight9.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ OK. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (por [**ejemplo, IDirect3DDevice9::SetLight).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
