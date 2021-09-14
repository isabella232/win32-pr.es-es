---
title: LVM_GETFOOTERITEMRECT mensaje (Commctrl.h)
description: Obtiene las coordenadas de un pie de página para un elemento especificado en un control de vista de lista. Envíe este mensaje explícitamente o mediante la macro \_ ListView GetFooterItemRect.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- LVM_GETFOOTERITEMRECT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974102"
---
# <a name="lvm_getfooteritemrect-message"></a>Mensaje \_ LVM GETFOOTERITEMRECT

Obtiene las coordenadas de un pie de página para un elemento especificado en un control de vista de lista. Envíe este mensaje explícitamente o mediante la macro [**\_ ListView GetFooterItemRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Índice del elemento en el control list-view.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) para recibir las coordenadas. La aplicación que realiza la llamada es responsable de asignar esta estructura. Las coordenadas recibidas se expresan como coordenadas de cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

