---
description: Devuelve un identificador de evento a un evento de combinación de prioridad que se está ejecutando actualmente.
ms.assetid: a7184459-7644-4e65-a8ea-13019889e02b
title: Método ID3DXAnimationController::GetCurrentPriorityBlend (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c02e65bb17e07b3d75c4949730141831e5b146011e77478d95c8976b792c1c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094560"
---
# <a name="id3dxanimationcontrollergetcurrentpriorityblend-method"></a>Método ID3DXAnimationController::GetCurrentPriorityBlend

Devuelve un identificador de evento a un evento de combinación de prioridad que se está ejecutando actualmente.

## <a name="syntax"></a>Sintaxis


```C++
D3DXEVENTHANDLE GetCurrentPriorityBlend();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para el evento de combinación de prioridad que se está ejecutando actualmente. **Se** devuelve NULL si no se está ejecutando ningún evento de combinación de prioridad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




