---
title: LVM_SCROLL mensaje (Commctrl.h)
description: Desplaza el contenido de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ Scroll.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- LVM_SCROLL controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05c3ed991cfc933a4436baf332b49c67a907b11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974066"
---
# <a name="lvm_scroll-message"></a>Mensaje LVM \_ SCROLL

Desplaza el contenido de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ Scroll.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de tipo **int** que especifica la cantidad de desplazamiento horizontal, en píxeles, con respecto a la posición actual del contenido de la vista de lista. Si el control list-view está en la vista de lista, este valor se redondea al número más cercano de píxeles que forman una columna completa.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor de tipo **int** que especifica la cantidad de desplazamiento vertical, en píxeles, con respecto a la posición actual del contenido de la vista de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente; de lo contrario, **FALSE**.

## <a name="remarks"></a>Observaciones

Cuando el control list-view está en la vista de informe, el control solo se puede desplazar verticalmente en incrementos de línea completa. Por lo tanto, *el parámetro lParam* se redondeará al número más cercano de píxeles que forman un incremento de línea completa. Por ejemplo, si el alto de una línea es de 16 píxeles y se pasa 8 para *lParam,* la lista se desplazará por 16 píxeles (1 línea). Si se pasa 7 para *lParam*, la lista se desplazará 0 píxeles (0 líneas).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





