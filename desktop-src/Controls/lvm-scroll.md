---
title: Mensaje de LVM_SCROLL (commctrl. h)
description: Desplaza el contenido de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro scroll de ListView.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- LVM_SCROLL controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491452"
---
# <a name="lvm_scroll-message"></a>Mensaje de desplazamiento del LVM \_

Desplaza el contenido de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ Scroll de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de tipo **int** que especifica la cantidad de desplazamiento horizontal, en píxeles, con respecto a la posición actual del contenido de la vista de lista. Si el control de vista de lista está en la vista de lista, este valor se redondea al número más cercano de píxeles que forman una columna completa.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor de tipo **int** que especifica la cantidad de desplazamiento vertical, en píxeles, con respecto a la posición actual del contenido de la vista de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true si es** correcto; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

Cuando el control de vista de lista está en la vista de informe, el control solo se puede desplazar verticalmente en incrementos de líneas completas. Por lo tanto, el parámetro *lParam* se redondea al número más cercano de píxeles que forman un incremento de línea completo. Por ejemplo, si el alto de una línea es 16 píxeles y 8 se pasa para *lParam*, la lista se desplazará por 16 píxeles (1 línea). Si se pasa 7 para *lParam*, la lista se desplazará 0 píxeles (0 líneas).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





