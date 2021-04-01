---
title: Mensaje de EM_NOSETFOCUS (commctrl. h)
description: Impide que un control de edición de una sola línea reciba el foco de teclado. Puede enviar este mensaje explícitamente o mediante la macro Edit \_ NoSetFocus.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- EM_NOSETFOCUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82830cda3402d2089d3421debaa7c4dbf13de5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150760"
---
# <a name="em_nosetfocus-message"></a>\_Mensaje NOSETFOCUS em

\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones de. Es posible que este mensaje no se admita en versiones futuras de Windows.\]

Impide que un control de edición de una sola línea reciba el foco de teclado. Puede enviar este mensaje explícitamente o mediante la macro [**Edit \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) .

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

Después de enviar este mensaje, el efecto es permanente.

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

[**Editar \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[**\_TAKEFOCUS em**](em-takefocus.md)
</dt> </dl>

 

 





