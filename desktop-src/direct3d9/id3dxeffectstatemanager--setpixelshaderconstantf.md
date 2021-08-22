---
description: 'Método ID3DXEffectStateManager::SetPixelShaderConstantF: una función de devolución de llamada que debe implementar un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.'
ms.assetid: db87ca8c-2539-4d80-854c-25b114a7e7e0
title: Método ID3DXEffectStateManager::SetPixelShaderConstantF (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6d92623bf97a05e5c398ee5e8b4a79b991a94aca5cf89e5a550f1c6c3f5c585d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044413"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstantf-method"></a>Método ID3DXEffectStateManager::SetPixelShaderConstantF

Función de devolución de llamada que debe implementar un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPixelShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartRegister* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de base cero del primer registro constante.

</dd> <dt>

*pConstantData* \[ out\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Matriz de constantes de punto flotante.

</dd> <dt>

*RegisterCount* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de registros en pConstantData.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ OK. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9::SetPixelShaderConstantF).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
