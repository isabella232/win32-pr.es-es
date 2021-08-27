---
title: HDM_GETOVERFLOWRECT mensaje (Commctrl.h)
description: Obtiene el rectángulo delimitador del botón de desbordamiento cuando el estilo HDS OVERFLOW se establece en el control de encabezado y el botón de desbordamiento \_ está visible. Envíe este mensaje explícitamente o mediante la \_ macro Header GetOverflowRect.
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- HDM_GETOVERFLOWRECT controles de Windows mensaje
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
ms.openlocfilehash: 0f48088ad6c4a1d8cc5b843eeafb167f790bdd8eac06c56e6cb74e8afc18d082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047055"
---
# <a name="hdm_getoverflowrect-message"></a>Mensaje \_ GETOVERFLOWRECT de HDM

Obtiene el rectángulo delimitador del botón de desbordamiento cuando el estilo [**HDS \_ OVERFLOW**](header-control-styles.md) se establece en el control de encabezado y el botón de desbordamiento está visible. Envíe este mensaje explícitamente o mediante la macro [**\_ Header GetOverflowRect.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa. Debe ser cero.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) para recibir la información del rectángulo delimitador. El remitente del mensaje es responsable de asignar esta estructura. Las coordenadas devueltas en la **estructura RECT** se expresan como coordenadas de pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente; de lo contrario, **FALSE**.

## <a name="remarks"></a>Comentarios

El control de encabezado debe tener el **estilo HDF \_ SPLITBUTTON**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Acerca de los controles de encabezado](header-controls.md)
</dt> </dl>

 

