---
title: Mensaje de LVM_GETSUBITEMRECT (commctrl. h)
description: Recupera información sobre el rectángulo delimitador de un subelemento de un control de vista de lista.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- LVM_GETSUBITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150889"
---
# <a name="lvm_getsubitemrect-message"></a>\_Mensaje GETSUBITEMRECT LVM

Recupera información sobre el rectángulo delimitador de un subelemento de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetSubItemRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) (recomendado). Este mensaje está pensado para usarse solo con controles de vista de lista que usan el estilo de [**\_ Informe LVS**](list-view-window-styles.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento primario del subelemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibirá la información del rectángulo delimitador del subelemento. Sus miembros se deben inicializar de acuerdo con las siguientes relaciones entre miembros y valores:



| Value                                                                                                                             | Significado                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**Arriba**</dt> </dl>    | Índice de base uno del subelemento.<br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**salido**</dt> </dl> | Valor de marca (vea la sección comentarios). Indica la parte del subelemento de vista de lista para el que se va a recuperar el rectángulo delimitador.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

A continuación se muestran los valores de marca que se pueden establecer.



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| **Valor de marca** | **Significado**                                                                                                         |
| límites de LVIR \_   | Devuelve el rectángulo delimitador del elemento completo, incluidos el icono y la etiqueta.                                    |
| icono de LVIR \_     | Devuelve el rectángulo delimitador del icono o del icono pequeño.                                                           |
| \_etiqueta LVIR    | Devuelve el rectángulo delimitador del elemento completo, incluidos el icono y la etiqueta. Es idéntico a los límites de LVIR \_ . |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

