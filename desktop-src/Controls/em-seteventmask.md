---
title: EM_SETEVENTMASK mensaje (Richedit.h)
description: Establece la máscara de evento para un control de edición enriquecido. La máscara de eventos especifica qué códigos de notificación envía el control a su ventana primaria.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- EM_SETEVENTMASK de mensajes controles de Windows
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
ms.openlocfilehash: 244274d969473531bae7c1d124af24a88d6b98d9db8bdbe073d054a3a9e36ac1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048505"
---
# <a name="em_seteventmask-message"></a>Mensaje \_ EM SETEVENTMASK

Establece la máscara de evento para un control de edición enriquecido. La máscara de eventos especifica qué códigos de notificación envía el control a su ventana primaria.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nueva máscara de evento para el control de edición enriquecido. Para obtener una lista de máscaras de eventos, vea [**Rich Edit Control Event Mask Flags**](rich-edit-control-event-mask-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve la máscara de evento anterior.

## <a name="remarks"></a>Comentarios

La máscara de evento predeterminada (antes de establecer ninguna) es ENM \_ NONE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETEVENTMASK**](em-geteventmask.md)
</dt> <dt>

[**Marcas de máscara de eventos del control Rich Edit**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





