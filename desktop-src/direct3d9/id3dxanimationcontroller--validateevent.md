---
description: Comprueba si un identificador de evento especificado es válido y el evento de animación aún no se ha completado.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: Método ID3DXAnimationController::ValidateEvent (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 24c5195d38aeaebefd1713df31f23b6b2ec7b2324a31381027f3442b541678c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094182"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a>Método ID3DXAnimationController::ValidateEvent

Comprueba si un identificador de evento especificado es válido y el evento de animación aún no se ha completado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hEvent* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para un evento de animación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve S \_ OK si el identificador de evento es válido y el evento aún no se ha completado.

Devuelve E \_ FAIL si el identificador del evento no es válido o el evento se ha completado.

## <a name="remarks"></a>Comentarios

El método indicará que un identificador de evento es válido incluso si el evento se está ejecutando pero aún no se ha completado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




