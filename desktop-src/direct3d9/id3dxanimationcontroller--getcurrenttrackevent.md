---
description: Devuelve un identificador de evento al evento que se ejecuta actualmente en la pista de animación especificada.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: Método ID3DXAnimationController::GetCurrentTrackEvent (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d61902765c29808941637d4ce7ebb7f4b361ac6904abc1fae5907738162347a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094516"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a>Método ID3DXAnimationController::GetCurrentTrackEvent

Devuelve un identificador de evento al evento que se ejecuta actualmente en la pista de animación especificada.

## <a name="syntax"></a>Sintaxis


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de seguimiento.

</dd> <dt>

*EventType* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXEVENT \_ TYPE**](./d3dxevent-type.md)**

Tipo de evento que se consulta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para el evento que se ejecuta actualmente en la pista especificada. **Se** devuelve NULL si no se ejecuta ningún evento en la pista especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
