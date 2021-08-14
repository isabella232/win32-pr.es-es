---
title: EN_OBJECTPOSITIONS de notificación (Richedit.h)
description: Notifica a la ventana primaria de un control de edición enriquecido cuando el control lee objetos . Un control de edición enriquecido envía este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- EN_OBJECTPOSITIONS código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3be6f3f41877a56396ef021e97130f4c174516160d7243144f10ea1dfd3951b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436702"
---
# <a name="en_objectpositions-notification-code"></a>Código de notificación EN \_ OBJECTPOSITIONS

Notifica a la ventana primaria de un control de edición enriquecido cuando el control lee objetos . Un control de edición enriquecido envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**OBJECTPOSITIONS.**](/windows/desktop/api/Richedit/ns-richedit-objectpositions)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para continuar con la **operación de** lectura.

Devuelve un valor distinto de cero para detener la **operación de** lectura.

## <a name="remarks"></a>Observaciones

Para recibir un código de notificación EN OBJECTPOSITIONS, especifique la marca \_ [**ENM \_ OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el [**mensaje EM \_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

