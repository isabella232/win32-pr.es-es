---
title: Mensaje de HDM_GETOVERFLOWRECT (commctrl. h)
description: Obtiene el rectángulo delimitador del botón de desbordamiento cuando el \_ estilo de desbordamiento de HDS se establece en el control de encabezado y el botón de desbordamiento está visible. Envíe este mensaje explícitamente o mediante la \_ macro header GetOverflowRect.
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- HDM_GETOVERFLOWRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534504"
---
# <a name="hdm_getoverflowrect-message"></a>HDM \_ GETOVERFLOWRECT

Obtiene el rectángulo delimitador del botón de desbordamiento cuando el estilo de [**\_ desbordamiento de HDS**](header-control-styles.md) se establece en el control de encabezado y el botón de desbordamiento está visible. Envíe este mensaje explícitamente o mediante la macro [**Header \_ GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza. Debe ser cero.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para recibir la información del rectángulo delimitador. El remitente del mensaje es responsable de la asignación de esta estructura. Las coordenadas devueltas en la estructura **Rect** se expresan como coordenadas de pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true si es** correcto; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

El control de encabezado debe tener el estilo **HDF \_ SPLITBUTTON**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Acerca de los controles de encabezado](header-controls.md)
</dt> </dl>

 

