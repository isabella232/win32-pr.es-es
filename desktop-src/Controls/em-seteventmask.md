---
title: EM_SETEVENTMASK mensaje (Richedit.h)
description: Establece la máscara de evento para un control de edición enriquecido. La máscara de eventos especifica qué códigos de notificación envía el control a su ventana primaria.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- EM_SETEVENTMASK controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4d79d23f7b56a29bc4f5142ed03b23e8081687
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062114"
---
# <a name="em_seteventmask-message"></a>Mensaje \_ SETEVENTMASK DE EM

Establece la máscara de evento para un control de edición enriquecido. La máscara de eventos especifica qué códigos de notificación envía el control a su ventana primaria.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nueva máscara de eventos para el control de edición enriquecido. Para obtener una lista de máscaras de eventos, vea [**Rich Edit Control Event Mask Flags**](rich-edit-control-event-mask-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve la máscara de evento anterior.

## <a name="remarks"></a>Observaciones

La máscara de evento predeterminada (antes de establecer ninguna) es ENM \_ NONE.

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

[**EM \_ GETEVENTMASK**](em-geteventmask.md)
</dt> <dt>

[**Marcas de máscara de eventos del control Rich Edit**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





