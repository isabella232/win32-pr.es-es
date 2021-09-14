---
title: LVM_GETITEMINDEXRECT mensaje (Commctrl.h)
description: Recupera el rectángulo delimitador para todo o parte de un subelemento en la vista actual de un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro ListView GetItemIndexRect.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- LVM_GETITEMINDEXRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ccd114713326c4796ca69f56fc2c38daf145db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061833"
---
# <a name="lvm_getitemindexrect-message"></a>Mensaje \_ GETITEMINDEXRECT de LVM

Recupera el rectángulo delimitador para todo o parte de un subelemento en la vista actual de un control de vista de lista. Envíe este mensaje explícitamente o mediante la macro [**\_ ListView GetItemIndexRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Puntero a una [**estructura LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) para el elemento primario del subelemento. El proceso de llamada es responsable de asignar esta estructura y establecer sus miembros. *wParam no* debe ser **NULL.**

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) para recibir las coordenadas. El proceso de llamada es responsable de asignar esta estructura. *lParam no* debe ser **NULL.** Establezca el **miembro** superior en el índice del subelemento. Establezca el **miembro** izquierdo en uno de los siguientes valores, lo que indica la parte del subelemento para el que se va a recuperar el rectángulo delimitador.



| Value                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**LÍMITES DE LVIR \_**</dt> </dl> | Devuelve el rectángulo delimitador de todo el subelemento, incluidos el icono y la etiqueta.<br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**ICONO \_ DE LVIR**</dt> </dl>       | Devuelve el rectángulo delimitador del icono o icono pequeño del subelemento.<br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**ETIQUETA \_ LVIR**</dt> </dl>    | Devuelve el rectángulo delimitador del texto del subelemento.<br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

