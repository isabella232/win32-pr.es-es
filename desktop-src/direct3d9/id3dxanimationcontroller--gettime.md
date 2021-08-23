---
description: Obtiene el tiempo de animación global.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: Método ID3DXAnimationController::GetTime (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6241bbd8c447889a4718369feabf8f26dacc73c58b8e6826c1797d0639422fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987835"
---
# <a name="id3dxanimationcontrollergettime-method"></a>Método ID3DXAnimationController::GetTime

Obtiene el tiempo de animación global.

## <a name="syntax"></a>Sintaxis


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Devuelve el tiempo de animación global.

## <a name="remarks"></a>Comentarios

Las animaciones se diseñan con una hora de animación local y se mezclan en la hora global [**con AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
