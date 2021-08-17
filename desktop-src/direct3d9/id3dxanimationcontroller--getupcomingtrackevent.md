---
description: Devuelve un identificador de evento al siguiente evento programado para producirse después de un evento especificado en una pista de animación.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: Método ID3DXAnimationController::GetUpcomingTrackEvent (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6e2730a9649400af8cc0229cb69ab695044681fde43a29a1a784d212f8d2641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279035"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a>Método ID3DXAnimationController::GetUpcomingTrackEvent

Devuelve un identificador de evento al siguiente evento programado para producirse después de un evento especificado en una pista de animación.

## <a name="syntax"></a>Sintaxis


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de seguimiento.

</dd> <dt>

*hEvent* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para un evento especificado después del cual se va a buscar un evento siguiente. Si se establece **en NULL,** el método devolverá el siguiente evento programado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para el siguiente evento programado para ejecutarse en la pista especificada. **Se** devuelve NULL si no se programa ningún evento nuevo.

## <a name="remarks"></a>Comentarios

Este método se puede usar de forma iterativa para buscar un evento deseado pasando repetidamente **NULL** para hEvent.

> [!Note]  
> No itere más después de que el método haya devuelto **NULL.**

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
