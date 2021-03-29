---
title: Mensaje de LVM_GETITEMINDEXRECT (commctrl. h)
description: Recupera el rectángulo delimitador para todo o parte de un subelemento en la vista actual de un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro GetItemIndexRect de ListView.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- LVM_GETITEMINDEXRECT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492413"
---
# <a name="lvm_getitemindexrect-message"></a>\_Mensaje GETITEMINDEXRECT LVM

Recupera el rectángulo delimitador para todo o parte de un subelemento en la vista actual de un control de vista de lista. Envíe este mensaje explícitamente o mediante la [**macro \_ GetItemIndexRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Puntero a una estructura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) para el elemento primario del subelemento. El proceso de llamada es responsable de asignar esta estructura y establecer sus miembros. *wParam* no debe ser **null**.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para recibir las coordenadas. El proceso de llamada es responsable de la asignación de esta estructura. *lParam* no debe ser **null**. Establezca el miembro **superior** en el índice del subelemento. Establezca el miembro **izquierdo** en uno de los siguientes valores, que indica la parte del subelemento para el que se va a recuperar el rectángulo delimitador.



| Value                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**límites de LVIR \_**</dt> </dl> | Devuelve el rectángulo delimitador del subelemento completo, incluidos el icono y la etiqueta.<br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**icono de LVIR \_**</dt> </dl>       | Devuelve el rectángulo delimitador del icono o el icono pequeño del subelemento.<br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**\_etiqueta LVIR**</dt> </dl>    | Devuelve el rectángulo delimitador del texto del subelemento.<br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

