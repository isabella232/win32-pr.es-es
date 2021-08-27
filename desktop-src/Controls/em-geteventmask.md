---
title: EM_GETEVENTMASK (Richedit.h)
description: Recupera la máscara de evento para un control de edición enriquecido. La máscara de eventos especifica qué códigos de notificación envía el control a su ventana primaria.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- EM_GETEVENTMASK controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4261869276015151e920e96e6c419675a1bce097384d6a918c2eac2b8005393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049235"
---
# <a name="em_geteventmask-message"></a>Mensaje \_ EM GETEVENTMASK

Recupera la máscara de evento para un control de edición enriquecido. La máscara de eventos especifica qué códigos de notificación envía el control a su ventana primaria.

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

Este mensaje devuelve la máscara de evento para el control de edición enriquecido.

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

[**Marcas de máscara de eventos del control Rich Edit**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





