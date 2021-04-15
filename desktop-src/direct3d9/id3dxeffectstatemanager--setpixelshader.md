---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer un sombreador de píxeles.
ms.assetid: 4124eff2-1d88-429c-b7ed-8d87155b5ddc
title: 'ID3DXEffectStateManager:: SetPixelShader (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 71a16bc267df95ed7efc1e0f74871b131e34ebe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547998"
---
# <a name="id3dxeffectstatemanagersetpixelshader-method"></a>ID3DXEffectStateManager:: SetPixelShader (método)

Una función de devolución de llamada que debe ser implementada por un usuario para establecer un sombreador de píxeles.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPixelShader(
  [in] LPDIRECT3DPIXELSHADER9 pShader
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pShader* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**

Un puntero a un objeto de sombreador de píxeles. Vea [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ correcto. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
