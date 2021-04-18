---
description: Obtiene el efecto administrador de estado.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'ID3DXEffect:: GetStateManager (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 293b642dfecfa4cc14426addf2567d43dffa7233
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707798"
---
# <a name="id3dxeffectgetstatemanager-method"></a>ID3DXEffect:: GetStateManager (método)

Obtiene el efecto administrador de estado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppManager* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***

Devuelve un puntero al administrador de Estados. Vea [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

[**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) es una interfaz implementada por el usuario que facilita las devoluciones de llamada en una aplicación para establecer el estado del dispositivo de un efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




