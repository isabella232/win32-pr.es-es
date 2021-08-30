---
title: LVM_GETITEMRECT mensaje (Commctrl.h)
description: Recupera el rectángulo delimitador para todo o parte de un elemento de la vista actual. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ GetItemRect.
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
ms.openlocfilehash: aad74047758011f841b21cc585b4df932f2d91cc4b1b661bb7a2bdeb045e19cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920075"
---
# <a name="lvm_getitemrect-message"></a>Mensaje \_ GETITEMRECT de LVM

Recupera el rectángulo delimitador para todo o parte de un elemento de la vista actual. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ GetItemRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Índice del elemento de vista de lista.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador. Cuando se envía el mensaje, **el** miembro izquierdo de esta estructura se usa para especificar la parte del elemento de vista de lista del que se va a recuperar el rectángulo delimitador. Debe establecerse en uno de los siguientes valores:



| Value                                                                                                                                                                     | Significado                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**LÍMITES DE LVIR \_**</dt> </dl>                   | Devuelve el rectángulo delimitador de todo el elemento, incluidos el icono y la etiqueta.<br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**ICONO \_ DE LVIR**</dt> </dl>                         | Devuelve el rectángulo delimitador del icono o icono pequeño.<br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**ETIQUETA \_ LVIR**</dt> </dl>                      | Devuelve el rectángulo delimitador del texto del elemento.<br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <dt>**LVIR \_ SELECTBOUNDS**</dt> </dl> | Devuelve la unión de los rectángulos ICON y LVIR LABEL de \_ LVIR, pero excluye las columnas de la vista de \_ informe.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

