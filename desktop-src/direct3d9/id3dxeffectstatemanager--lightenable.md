---
description: Función de devolución de llamada que debe implementar un usuario para habilitar o deshabilitar una luz.
ms.assetid: 11522ca3-8a2f-4767-a6e6-4186cb4f3115
title: Método ID3DXEffectStateManager::LightEnable (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.LightEnable
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0a7ce5a4fe90e911faaf8927fe584004eec7a68eae7b5c75f1c3a92f017fd4bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295790"
---
# <a name="id3dxeffectstatemanagerlightenable-method"></a>Método ID3DXEffectStateManager::LightEnable

Función de devolución de llamada que debe implementar un usuario para habilitar o deshabilitar una luz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LightEnable(
  [in] DWORD Index,
  [in] BOOL  Enable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de base cero de la luz. Este es el mismo índice de [**IDirect3DDevice9::SetLight.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)

</dd> <dt>

*Habilitar* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

True para habilitar la luz; en caso contrario, false.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ OK. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (por [**ejemplo, IDirect3DDevice9::LightEnable).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
