---
description: Obtiene el peso de combinación de prioridad actual utilizado por el controlador de animación.
ms.assetid: ceaf611e-e85b-4958-b8ac-7e60b98b1aad
title: Método ID3DXAnimationController::GetPriorityBlend (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c27e4c6d2cc706b30f2be99030e7bb4a5bccf209
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569924"
---
# <a name="id3dxanimationcontrollergetpriorityblend-method"></a>Método ID3DXAnimationController::GetPriorityBlend

Obtiene el peso de combinación de prioridad actual utilizado por el controlador de animación.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT GetPriorityBlend();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Devuelve el peso de combinación de prioridad actual.

## <a name="remarks"></a>Observaciones

El peso de combinación de prioridad se usa para combinar pistas de prioridad alta y baja.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
