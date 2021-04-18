---
description: Función de devolución de llamada que debe ser implementada por un usuario para establecer el estado de representación.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'ID3DXEffectStateManager:: SetRenderState (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 111ab8ff379d5b095500101674fc45b6a2b31bc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718302"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a>ID3DXEffectStateManager:: SetRenderState (método)

Función de devolución de llamada que debe ser implementada por un usuario para establecer el estado de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Estado* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**

Estado de representación que se va a establecer. [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

</dd> <dt>

*Valor* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Valor de estado de representación. Consulte [Estados de efectos (Direct3D 9)](effect-states.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ correcto. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
