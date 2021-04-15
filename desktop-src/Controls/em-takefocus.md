---
title: Mensaje de EM_TAKEFOCUS (commctrl. h)
description: Fuerza un control de edición de una sola línea para recibir el foco de teclado. Puede enviar este mensaje explícitamente o mediante la macro Edit \_ TakeFocus.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- EM_TAKEFOCUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_TAKEFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4abdf926cdd337760b5cf151c3f8ee08cb418b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490720"
---
# <a name="em_takefocus-message"></a>\_Mensaje TAKEFOCUS em

\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones de. Es posible que este mensaje no se admita en versiones futuras de Windows.\]

Fuerza un control de edición de una sola línea para recibir el foco de teclado. Puede enviar este mensaje explícitamente o mediante la macro [**Edit \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) .

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

No se utiliza el valor devuelto.

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

El uso de este mensaje podría poner en peligro la seguridad del programa.

## <a name="remarks"></a>Observaciones

Este mensaje se omite si el control de edición no es un control de edición de una sola línea.

Si el control de edición ha recibido previamente un mensaje [**\_ NOSETFOCUS em**](em-nosetfocus.md) , parecerá que el control de edición tiene el foco sin tenerlo realmente; de lo contrario, el control de edición recibirá el foco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**Editar \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[**\_NOSETFOCUS em**](em-nosetfocus.md)
</dt> </dl>

 

 





