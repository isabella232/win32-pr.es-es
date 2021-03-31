---
title: Mensaje EM_GETEVENTMASK (RichEdit. h)
description: Recupera la máscara de eventos para un control Rich Edit. La máscara de eventos especifica los códigos de notificación que el control envía a su ventana primaria.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- EM_GETEVENTMASK controles de mensajes de Windows
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
ms.openlocfilehash: 4f4d231bbb9d5592ff2f90da6a5096783b38c292
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996753"
---
# <a name="em_geteventmask-message"></a>\_Mensaje GETEVENTMASK (EM

Recupera la máscara de eventos para un control Rich Edit. La máscara de eventos especifica los códigos de notificación que el control envía a su ventana primaria.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve la máscara de eventos para el control Rich Edit.

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

[**una \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**Marcas de máscara de eventos de control de edición enriquecida**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





