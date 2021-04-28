---
description: 'Método ID3DXEffectStateManager::SetPixelShaderConstantB: una función de devolución de llamada que debe implementar un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.'
ms.assetid: ad4d9beb-fd34-4574-9787-61bd3bfaaaaa
title: Método ID3DXEffectStateManager::SetPixelShaderConstantB (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ace60b72345c992c3f35943362f6a0958f043aba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090493"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstantb-method"></a>Método ID3DXEffectStateManager::SetPixelShaderConstantB

Función de devolución de llamada que debe implementar un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPixelShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
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

Tipo: **const [**BOOL**](../winprog/windows-data-types.md) \***

Matriz de constantes booleanas.

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
-   Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9::SetPixelShaderConstantB).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
