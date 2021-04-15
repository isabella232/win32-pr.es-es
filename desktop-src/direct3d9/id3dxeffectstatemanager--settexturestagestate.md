---
description: Función de devolución de llamada que debe ser implementada por un usuario para establecer el estado de la fase de textura.
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: 'ID3DXEffectStateManager:: SetTextureStageState (método) (D3DX9Effect. h)'
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
ms.openlocfilehash: 937fd3f2b89dc093d9dceb9441f53d6be2cb06b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678831"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a>ID3DXEffectStateManager:: SetTextureStageState (método)

Función de devolución de llamada que debe ser implementada por un usuario para establecer el estado de la fase de textura.

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

*Stage* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Fase a la que se asigna la textura. Este es el valor de índice en [**IDirect3DDevice9:: SetTexture**](/windows/desktop/api) o [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).

</dd> <dt>

*Tipo* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**

Define el tipo de operación que realizará una fase de textura. Vea [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).

</dd> <dt>

*Valor* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Puede ser una operación ([**D3DTEXTUREOP**](./d3dtextureop.md)) o un valor de argumento ([D3DTA](d3dta.md)), en función de lo que se elija para el tipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ correcto. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
