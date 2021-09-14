---
description: Función de devolución de llamada que debe implementar un usuario para establecer un sampler.
ms.assetid: 1e19e8cd-341d-4372-9182-8b3c82155407
title: Método ID3DXEffectStateManager::SetSamplerState (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetSamplerState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bba12db8dbc1902adc5c64b4cc1726e081dfea70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060618"
---
# <a name="id3dxeffectstatemanagersetsamplerstate-method"></a>Método ID3DXEffectStateManager::SetSamplerState

Función de devolución de llamada que debe implementar un usuario para establecer un sampler.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSamplerState(
  [in] DWORD               Sampler,
  [in] D3DSAMPLERSTATETYPE Type,
  [in] DWORD               Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Sampler* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de sampler de base cero.

</dd> <dt>

*Tipo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**

Identifica el estado del muestreador, que puede especificar el filtrado, el direccionamiento o el color del borde. Vea [**D3DSAMPLERSTATETYPE.**](./d3dsamplerstatetype.md)

</dd> <dt>

*Valor* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Valor de uno de los tipos de estado del muestreador en Tipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ OK. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9::SetSamplerState).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
