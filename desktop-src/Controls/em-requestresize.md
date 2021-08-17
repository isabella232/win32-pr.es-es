---
title: EM_REQUESTRESIZE mensaje (Richedit.h)
description: Fuerza a un control de edición enriquecido a enviar un código de notificación EN \_ REQUESTRESIZE a su ventana primaria.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- EM_REQUESTRESIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7113f52e2fa3a293549443f779ba937bf20b85736c6751cd9ab77bdbecd45c3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440165"
---
# <a name="em_requestresize-message"></a>Mensaje \_ EM REQUESTRESIZE

Fuerza a un control de edición enriquecido a enviar un código de notificación [**EN \_ REQUESTRESIZE**](en-requestresize.md) a su ventana primaria.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este mensaje es útil durante el [**procesamiento de WM \_ SIZE**](/windows/desktop/winmsg/wm-size) para el elemento primario de un control de edición enriquecido sin fondo.

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

[**EN \_ REQUESTRESIZE**](en-requestresize.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**TAMAÑO \_ WM**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

