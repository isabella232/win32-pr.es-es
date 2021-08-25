---
description: Devuelve un identificador de evento al siguiente evento blend de prioridad programado para producirse después de un evento especificado.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: Método ID3DXAnimationController::GetUpcomingPriorityBlend (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c58bf5e2a8736db98e0461988f984709e756d269d09c74dd673356676702ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849085"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a>Método ID3DXAnimationController::GetUpcomingPriorityBlend

Devuelve un identificador de evento al siguiente evento blend de prioridad programado para producirse después de un evento especificado.

## <a name="syntax"></a>Sintaxis


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hEvent* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para un evento especificado después del cual se va a buscar un evento blend de prioridad siguiente. Si se establece **en NULL,** el método devolverá el siguiente evento de combinación de prioridad programada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para el siguiente evento de combinación de prioridad programada. **Se** devuelve NULL si no se programa ningún nuevo evento de combinación de prioridad.

## <a name="remarks"></a>Comentarios

Este método se puede usar de forma iterativa para buscar un evento de combinación de prioridad deseado pasando repetidamente **NULL** para hEvent.

> [!Note]  
> No itere más después de que el método haya devuelto **NULL.**

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




