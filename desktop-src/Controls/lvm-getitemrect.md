---
title: Mensaje de LVM_GETITEMRECT (commctrl. h)
description: Recupera el rectángulo delimitador para todo o parte de un elemento de la vista actual. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemRect de ListView.
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- LVM_GETITEMRECT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079654"
---
# <a name="lvm_getitemrect-message"></a>\_Mensaje GETITEMRECT LVM

Recupera el rectángulo delimitador para todo o parte de un elemento de la vista actual. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Índice del elemento de vista de lista.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador. Cuando se envía el mensaje, el miembro **izquierdo** de esta estructura se usa para especificar la parte del elemento de vista de lista de la que se va a recuperar el rectángulo delimitador. Debe establecerse en uno de los siguientes valores:



| Value                                                                                                                                                                     | Significado                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**límites de LVIR \_**</dt> </dl>                   | Devuelve el rectángulo delimitador del elemento completo, incluidos el icono y la etiqueta.<br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**icono de LVIR \_**</dt> </dl>                         | Devuelve el rectángulo delimitador del icono o del icono pequeño.<br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**\_etiqueta LVIR**</dt> </dl>                      | Devuelve el rectángulo delimitador del texto del elemento.<br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <dt>**LVIR \_ SELECTBOUNDS**</dt> </dl> | Devuelve la Unión del icono de LVIR \_ y los \_ rectángulos de etiqueta de LVIR, pero excluye las columnas en la vista de informe.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

