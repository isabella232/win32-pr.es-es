---
title: HDM_ORDERTOINDEX mensaje (Commctrl.h)
description: Recupera un valor de índice para un elemento en función de su orden en el control de encabezado. Puede enviar este mensaje explícitamente o usar la \_ macro OrderToIndex de encabezado.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- HDM_ORDERTOINDEX controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061979"
---
# <a name="hdm_ordertoindex-message"></a>Mensaje \_ ORDERTOINDEX de HDM

Recupera un valor de índice para un elemento en función de su orden en el control de encabezado. Puede enviar este mensaje explícitamente o usar la macro [**\_ OrderToIndex de**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) encabezado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Orden en el que el elemento aparece dentro del control de encabezado, de izquierda a derecha. Por ejemplo, el valor de índice del elemento en la columna del extremo izquierdo sería 0. El valor del siguiente elemento a la derecha sería 1, y así sucesivamente.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve INT que indica el índice del elemento. Si *wParam no es* válido (negativo o demasiado grande), el valor devuelto es igual a *wParam.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





