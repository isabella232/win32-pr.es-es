---
title: Mensaje de LVM_GETFOOTERITEMRECT (commctrl. h)
description: Obtiene las coordenadas de un pie de página para un elemento especificado en un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro GetFooterItemRect de ListView.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- LVM_GETFOOTERITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274508"
---
# <a name="lvm_getfooteritemrect-message"></a>\_Mensaje GETFOOTERITEMRECT LVM

Obtiene las coordenadas de un pie de página para un elemento especificado en un control de vista de lista. Envíe este mensaje explícitamente o mediante la [**macro \_ GetFooterItemRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Índice del elemento en el control de vista de lista.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para recibir las coordenadas. La aplicación que realiza la llamada es responsable de la asignación de esta estructura. Las coordenadas recibidas se expresan como coordenadas de cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

