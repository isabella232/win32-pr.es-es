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
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062139"
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
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EN \_ REQUESTRESIZE**](en-requestresize.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**TAMAÑO \_ DE WM**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

