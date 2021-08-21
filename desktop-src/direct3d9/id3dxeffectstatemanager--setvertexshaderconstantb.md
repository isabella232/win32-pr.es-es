---
description: 'Método ID3DXEffectStateManager::SetVertexShaderConstantB: una función de devolución de llamada que debe implementar un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.'
ms.assetid: 25fd0c68-11b5-4401-a2f8-86075ba3fa54
title: Método ID3DXEffectStateManager::SetVertexShaderConstantB (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0db8c141f16a14db57e5d6867a9894399bacf5a5cebb7c7e14a2592ea7f09bff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121441"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a>Método ID3DXEffectStateManager::SetVertexShaderConstantB

Función de devolución de llamada que debe implementar un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetVertexShaderConstantB(
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
-   Se producirá un error en la llamada de estado de efecto dinámico (por [**ejemplo, IDirect3DDevice9::SetVertexShaderConstantB).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
