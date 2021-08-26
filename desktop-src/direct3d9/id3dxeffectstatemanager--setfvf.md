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
ms.openlocfilehash: 828f6873ed9bf48de6a02d4195fdd1fa9d2bc39f99da1f8906fd8a2c53075cf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026415"
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
-   Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9::SetFVF).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
