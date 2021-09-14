---
description: Función de devolución de llamada que debe implementar un usuario para establecer el estado del material.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: Método ID3DXEffectStateManager::SetMaterial (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b503bd195468fb323e7e655c0bdd201e25dfdce2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060624"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a>Método ID3DXEffectStateManager::SetMaterial

Función de devolución de llamada que debe implementar un usuario para establecer el estado del material.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMaterial* \[ En\]
</dt> <dd>

Tipo: **const [**D3DMATERIAL9**](d3dmaterial9.md) \***

Puntero al estado del material. Vea [**D3DMATERIAL9.**](d3dmaterial9.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El método implementado por el usuario debe devolver S \_ OK. Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:

-   Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   Se producirá un error en la llamada de estado de efecto dinámico (por [**ejemplo, IDirect3DDevice9::SetMaterial).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
