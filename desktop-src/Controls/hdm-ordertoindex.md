---
title: Mensaje de HDM_ORDERTOINDEX (commctrl. h)
description: Recupera un valor de índice para un elemento en función de su orden en el control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header OrderToIndex.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- HDM_ORDERTOINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b65d10fb27c9a07639ebbd5770a53d72cbf0aba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079308"
---
# <a name="hdm_ordertoindex-message"></a>HDM \_ ORDERTOINDEX

Recupera un valor de índice para un elemento en función de su orden en el control de encabezado. Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El orden en el que aparece el elemento dentro del control de encabezado, de izquierda a derecha. Por ejemplo, el valor de índice del elemento en la columna de la izquierda es 0. El valor del siguiente elemento a la derecha sería 1, y así sucesivamente.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que indica el índice del elemento. Si *wParam* no es válido (negativo o demasiado grande), el valor devuelto es igual a *wParam*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





