---
description: Establece el peso de fusión de prioridad para la pista de animación especificada.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'ID3DXAnimationController:: SetTrackPriority (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 32f1f8cce4641203782b0a84840d2986780da26a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718533"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a>ID3DXAnimationController:: SetTrackPriority (método)

Establece el peso de fusión de prioridad para la pista de animación especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador de seguimiento.

</dd> <dt>

*Prioridad* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DXPRIORITY \_ Type**](./d3dxpriority-type.md)**

Prioridad de la pista. Este parámetro debe establecerse en una de las constantes de [**\_ tipo D3DXPRIORITY**](./d3dxpriority-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
