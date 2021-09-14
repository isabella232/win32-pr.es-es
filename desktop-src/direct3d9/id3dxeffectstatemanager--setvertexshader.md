---
description: Función de devolución de llamada que debe implementar un usuario para establecer un sombreador de vértices.
ms.assetid: 8f3d3be3-c073-441d-a318-6d2cd5e7aca5
title: Método ID3DXEffectStateManager::SetVertexShader (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9fd25158f2aa6ab0a22d6226e8e709c3b498b0e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060613"
---
# <a name="id3dxeffectstatemanagersetvertexshader-method"></a>Método ID3DXEffectStateManager::SetVertexShader

Función de devolución de llamada que debe implementar un usuario para establecer un sombreador de vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetVertexShader(
  [in] LPDIRECT3DVERTEXSHADER9 pShader
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pShader* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**

Puntero a un objeto de sombreador de vértices. Vea [**IDirect3DVertexShader9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ OK. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9::SetVertexShader).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
