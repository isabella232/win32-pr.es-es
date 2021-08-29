---
title: WM_NOTIFYFORMAT mensaje (Winuser.h)
description: Determina si una ventana acepta estructuras ANSI o Unicode en el mensaje de notificación \_ WM NOTIFY. Los \_ mensajes DE WM NOTIFYFORMAT se envían desde un control común a su ventana primaria y desde la ventana primaria al control común.
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- WM_NOTIFYFORMAT controles de Windows mensaje
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05cb41a88bffd7cc4ca3b406017dd08e297a239823fc2f5727be844b58e4bdfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077679"
---
# <a name="wm_notifyformat-message"></a>Mensaje \_ DE WM NOTIFYFORMAT

Determina si una ventana acepta estructuras ANSI o Unicode en el [**mensaje de notificación WM \_ NOTIFY.**](wm-notify.md) **WM \_ Los mensajes NOTIFYFORMAT** se envían desde un control común a su ventana primaria y desde la ventana primaria al control común.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana que envía el **mensaje \_ WM NOTIFYFORMAT.** Si *lParam es* NF \_ QUERY, este parámetro es el identificador de un control. Si *lParam es* NF \_ REQUERY, este parámetro es el identificador de la ventana primaria de un control.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor de comando que especifica la naturaleza del **mensaje \_ WM NOTIFYFORMAT.** Este será uno de los siguientes valores:



| Valor                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <dt>**CONSULTA \_ NF**</dt> </dl>       | El mensaje es una consulta para determinar si se deben usar estructuras ANSI o Unicode en [**mensajes WM \_ NOTIFY.**](wm-notify.md) Este comando se envía desde un control a su ventana primaria durante la creación de un control y en respuesta a un comando \_ REQUERY de NF.<br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <dt>**NF \_ REQUERY**</dt> </dl> | El mensaje es una solicitud para que un control envíe un formulario NF QUERY de este mensaje a \_ su ventana primaria. Este comando se envía desde la ventana primaria. La ventana primaria pide al control que vuelva a consultarlo sobre el tipo de estructuras que se van a usar en [**los mensajes \_ WM NOTIFY.**](wm-notify.md) Si *lParam es* NF \_ REQUERY, el valor devuelto es el resultado de la operación de reconsulta.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                                 | Descripción                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ANSI \_ de NFR**</dt> </dl>    | Las estructuras ANSI deben usarse en [**los mensajes \_ WM NOTIFY**](wm-notify.md) enviados por el control .<br/>     |
| <dl> <dt>**NFR \_ UNICODE**</dt> </dl> | Las estructuras Unicode deben usarse en [**los mensajes \_ WM NOTIFY**](wm-notify.md) enviados por el control . <br/> |
| <dl> <dt>**0**</dt> </dl>            | Se produjo un error.<br/>                                                                                  |



 

## <a name="remarks"></a>Comentarios

Cuando se crea un control común, el control envía un mensaje **DE WM \_ NOTIFYFORMAT** a su ventana primaria para determinar el tipo de estructuras que se usarán en los [**mensajes WM \_ NOTIFY.**](wm-notify.md) Si la ventana primaria no controla este mensaje, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) responde según el tipo de la ventana primaria. Es decir, si la ventana primaria es una ventana Unicode, **DefWindowProc** devuelve UNICODE NFR y, si la ventana primaria es una ventana \_ ANSI, **DefWindowProc** devuelve NFR \_ ANSI. Si la ventana primaria es un cuadro de diálogo y no controla este mensaje, la función [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) responde de forma similar según el tipo del cuadro de diálogo (Unicode o ANSI).

Una ventana primaria puede cambiar el tipo de estructuras que un control común usa en los mensajes [**WM \_ NOTIFY**](wm-notify.md) estableciendo *lParam* en NF REQUERY y enviando un mensaje \_ WM **\_ NOTIFYFORMAT** al control. Esto hace que el control envíe un formulario NF \_ QUERY del mensaje WM **\_ NOTIFYFORMAT** a la ventana primaria.

Todos los controles comunes enviarán **mensajes \_ WM NOTIFYFORMAT.** Sin embargo, los controles Windows estándar (controles de edición, cuadros combinados, cuadros de lista, botones, barras de desplazamiento y controles estáticos) no lo hacen.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

