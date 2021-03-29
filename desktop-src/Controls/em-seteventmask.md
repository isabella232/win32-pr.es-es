---
title: Mensaje EM_SETEVENTMASK (RichEdit. h)
description: Establece la máscara de eventos para un control Rich Edit. La máscara de eventos especifica los códigos de notificación que el control envía a su ventana primaria.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- EM_SETEVENTMASK controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492460"
---
# <a name="em_seteventmask-message"></a>\_Mensaje em SETEVENTMASK

Establece la máscara de eventos para un control Rich Edit. La máscara de eventos especifica los códigos de notificación que el control envía a su ventana primaria.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nueva máscara de eventos para el control Rich Edit. Para obtener una lista de máscaras de eventos, vea [**marcas de máscara de eventos de control de edición enriquecida**](rich-edit-control-event-mask-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve la máscara de eventos anterior.

## <a name="remarks"></a>Observaciones

La máscara de eventos predeterminada (antes de que se establezca) es ENM \_ None.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_GETEVENTMASK (EM**](em-geteventmask.md)
</dt> <dt>

[**Marcas de máscara de eventos de control de edición enriquecida**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





