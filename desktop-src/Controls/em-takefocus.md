---
title: EM_TAKEFOCUS mensaje (Commctrl.h)
description: Fuerza a un control de edición de una sola línea a recibir el foco del teclado. Puede enviar este mensaje explícitamente o mediante la macro Edit \_ TakeFocus .
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- EM_TAKEFOCUS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062041"
---
# <a name="em_takefocus-message"></a>Mensaje \_ EM TAKEFOCUS

\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones. Es posible que este mensaje no se pueda usar en versiones futuras de Windows.\]

Fuerza a un control de edición de una sola línea a recibir el foco del teclado. Puede enviar este mensaje explícitamente o mediante la [**macro Edit \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) .

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

No se usa el valor devuelto.

## <a name="security-considerations"></a>Consideraciones de seguridad

El uso de este mensaje podría poner en peligro la seguridad del programa.

## <a name="remarks"></a>Observaciones

Este mensaje se omite si el control de edición no es un control de edición de una sola línea.

Si el control de edición recibió previamente un mensaje [**\_ EM NOSETFOCUS,**](em-nosetfocus.md) el control de edición parecerá tener el foco sin tener realmente el foco; de lo contrario, el control de edición recibirá el foco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**Editar \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[**EM \_ NOSETFOCUS**](em-nosetfocus.md)
</dt> </dl>

 

 





