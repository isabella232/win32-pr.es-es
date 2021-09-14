---
title: EM_NOSETFOCUS mensaje (Commctrl.h)
description: Impide que un control de edición de una sola línea reciba el foco del teclado. Puede enviar este mensaje explícitamente o mediante la macro Edit \_ NoSetFocus .
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- EM_NOSETFOCUS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062155"
---
# <a name="em_nosetfocus-message"></a>Mensaje \_ EM NOSETFOCUS

\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones. Es posible que este mensaje no se pueda usar en versiones futuras de Windows.\]

Impide que un control de edición de una sola línea reciba el foco del teclado. Puede enviar este mensaje explícitamente o mediante la [**macro Edit \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) .

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

Una vez enviado este mensaje, el efecto es permanente.

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

[**Editar \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[**EM \_ TAKEFOCUS**](em-takefocus.md)
</dt> </dl>

 

 





