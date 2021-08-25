---
description: Establece el peso de combinación de prioridad para la pista de animación especificada.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: Método ID3DXAnimationController::SetTrackPriority (D3dx9anim.h)
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
ms.openlocfilehash: be294710fcd6ec2d8e72c7d7c9437623d29a2729a52144d4edfdc91e5be7eea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848975"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a>Método ID3DXAnimationController::SetTrackPriority

Establece el peso de combinación de prioridad para la pista de animación especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de seguimiento.

</dd> <dt>

*Prioridad* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md)**

Seguimiento de la prioridad. Este parámetro debe establecerse en una de las constantes de [**D3DXPRIORITY \_ TYPE**](./d3dxpriority-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
