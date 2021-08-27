---
title: UDM_GETPOS32 mensaje (Commctrl.h)
description: Devuelve la posición de 32 bits de un control de arriba a abajo.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- UDM_GETPOS32 controles de Windows mensaje
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11d043ca4f6b69a554b43d5abeaf35e4c2a2a6d72797e829900529df70b6c47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059795"
---
# <a name="udm_getpos32-message"></a>Mensaje \_ GETPOS32 de UDM

Devuelve la posición de 32 bits de un control de arriba a abajo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un **valor BOOL** que se establece en cero si el valor se recupera correctamente o distinto de cero si se produce un error. Si este parámetro se establece en **NULL,** no se notifican los errores.

Si **se usa \_ UDM GETPOS32** en una situación entre procesos, este parámetro debe ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la posición de un control de flecha hacia abajo con precisión de 32 bits. Las aplicaciones deben comprobar el *valor lParam* para determinar si el valor devuelto es válido.

## <a name="remarks"></a>Comentarios

Cuando procesa este mensaje, el control de flechas actualiza su posición actual en función del título de la ventana del compañero. Devuelve un error si no hay ninguna ventana de compañeros o si el título especifica un valor no válido o fuera del intervalo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ SETPOS32**](udm-setpos32.md)
</dt> </dl>

 

 





