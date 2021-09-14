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
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964916"
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

## <a name="remarks"></a>Observaciones

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

 

 
