---
title: Mensaje de HDM_GETITEMRECT (commctrl. h)
description: Obtiene el rectángulo delimitador de un elemento determinado en un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header GetItemRect.
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- HDM_GETITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491476"
---
# <a name="hdm_getitemrect-message"></a>HDM \_ GETITEMRECT

Obtiene el rectángulo delimitador de un elemento determinado en un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Índice de base cero del elemento de control de encabezado para el que se va a recuperar el rectángulo delimitador.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**Rect**](/windows/win32/api/windef/ns-windef-rect) que recibe la información del rectángulo delimitador. El remitente del mensaje es responsable de la asignación de esta estructura. Las coordenadas devueltas en la estructura RECT se expresan en relación con el elemento primario del control de encabezado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





