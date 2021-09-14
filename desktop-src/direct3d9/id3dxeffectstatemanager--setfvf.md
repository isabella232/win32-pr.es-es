---
description: Función de devolución de llamada que debe implementar un usuario para establecer un código FVF.
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: Método ID3DXEffectStateManager::SetFVF (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetFVF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a68ab07e4f486a8df80ecde5844739a6a010c2dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060626"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a>Método ID3DXEffectStateManager::SetFVF

Función de devolución de llamada que debe implementar un usuario para establecer un código FVF.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FVF* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Constante FVF, que determina cómo interpretar los datos de vértice. Vea [D3DFVF](d3dfvf.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ OK. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (por [**ejemplo, IDirect3DDevice9::SetFVF).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
