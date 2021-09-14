---
title: LVM_GETITEMRECT mensaje (Commctrl.h)
description: Recupera el rectángulo delimitador para todo o parte de un elemento de la vista actual. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetItemRect.
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- LVM_GETITEMRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061830"
---
# <a name="lvm_getitemrect-message"></a>Mensaje \_ GETITEMRECT de LVM

Recupera el rectángulo delimitador para todo o parte de un elemento de la vista actual. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetItemRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Índice del elemento list-view.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador. Cuando se envía el mensaje, **se** usa el miembro izquierdo de esta estructura para especificar la parte del elemento de vista de lista del que se va a recuperar el rectángulo delimitador. Debe establecerse en uno de los siguientes valores:



| Value                                                                                                                                                                     | Significado                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**LÍMITES DE LVIR \_**</dt> </dl>                   | Devuelve el rectángulo delimitador de todo el elemento, incluidos el icono y la etiqueta.<br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**ICONO \_ DE LVIR**</dt> </dl>                         | Devuelve el rectángulo delimitador del icono o icono pequeño.<br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**ETIQUETA \_ LVIR**</dt> </dl>                      | Devuelve el rectángulo delimitador del texto del elemento.<br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <dt>**LVIR \_ SELECTBOUNDS**</dt> </dl> | Devuelve la unión de los rectángulos LVIR \_ ICON y LVIR \_ LABEL, pero excluye las columnas de la vista de informe.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

