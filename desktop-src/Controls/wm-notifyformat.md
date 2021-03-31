---
title: Mensaje de WM_NOTIFYFORMAT (Winuser. h)
description: Determina si una ventana acepta estructuras ANSI o Unicode en el \_ mensaje de notificación de notificaciones de WM. \_Los mensajes NOTIFYFORMAT de WM se envían desde un control común a su ventana primaria y desde la ventana primaria al control común.
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- WM_NOTIFYFORMAT controles de mensajes de Windows
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
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996634"
---
# <a name="wm_notifyformat-message"></a>Mensaje de NOTIFYFORMAT de WM \_

Determina si una ventana acepta estructuras ANSI o Unicode en el mensaje de notificación de [**\_ notificaciones de WM**](wm-notify.md) . **WM \_** Los mensajes NOTIFYFORMAT se envían desde un control común a su ventana primaria y desde la ventana primaria al control común.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana que está enviando el mensaje **de \_ NOTIFYFORMAT de WM** . Si *lParam* es \_ una consulta de NF, este parámetro es el identificador de un control. Si *lParam* es \_ la reconsulta de NF, este parámetro es el identificador de la ventana primaria de un control.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor del comando que especifica la naturaleza del mensaje **de \_ NOTIFYFORMAT de WM** . Este será uno de los siguientes valores:



| Value                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <dt>**NF ( \_ consulta)**</dt> </dl>       | El mensaje es una consulta para determinar si se deben usar estructuras ANSI o Unicode en los mensajes de [**\_ notificación de WM**](wm-notify.md) . Este comando se envía desde un control a su ventana primaria durante la creación de un control y en respuesta a un \_ comando de REquery de NF.<br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <dt>**\_nueva consulta de NF**</dt> </dl> | El mensaje es una solicitud para que un control envíe un \_ formulario de consulta de NF de este mensaje a su ventana primaria. Este comando se envía desde la ventana primaria. La ventana primaria pide al control que vuelva a consultarlo sobre el tipo de estructuras que se va a usar en los mensajes de [**\_ notificación de WM**](wm-notify.md) . Si *lParam* es la \_ reconsulta de NF, el valor devuelto es el resultado de la operación de reconsulta.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                                 | Descripción                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ANSI NFR**</dt> </dl>    | Las estructuras ANSI deben usarse en los mensajes de [**\_ notificación de WM**](wm-notify.md) enviados por el control.<br/>     |
| <dl> <dt>**Unicode NFR \_**</dt> </dl> | Las estructuras Unicode se deben usar en los mensajes de [**\_ notificación de WM**](wm-notify.md) enviados por el control. <br/> |
| <dl> <dt>**0,1**</dt> </dl>            | Se produjo un error.<br/>                                                                                  |



 

## <a name="remarks"></a>Observaciones

Cuando se crea un control común, el control envía un mensaje de **WM \_ NOTIFYFORMAT** a su ventana primaria para determinar el tipo de estructuras que se van a usar en los mensajes de [**\_ notificación de WM**](wm-notify.md) . Si la ventana primaria no controla este mensaje, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) responde según el tipo de la ventana primaria. Es decir, si la ventana primaria es una ventana Unicode, **DefWindowProc** devuelve \_ Unicode NFR y, si la ventana primaria es una ventana ANSI, **DEFWINDOWPROC** devuelve el \_ ANSI NFR. Si la ventana primaria es un cuadro de diálogo y no controla este mensaje, la función [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) responde de forma similar según el tipo de cuadro de diálogo (Unicode o ANSI).

Una ventana primaria puede cambiar el tipo de estructuras que usa un control común en los mensajes de [**\_ notificación de WM**](wm-notify.md) si establece *lParam* en NF \_ Requery y envía un mensaje de **WM \_ NOTIFYFORMAT** al control. Esto hace que el control envíe un \_ formulario de consulta de NF del mensaje de **\_ NOTIFYFORMAT de WM** a la ventana primaria.

Todos los controles comunes enviarán mensajes de **WM \_ NOTIFYFORMAT** . Sin embargo, los controles estándar de Windows (controles de edición, cuadros combinados, cuadros de lista, botones, barras de desplazamiento y controles estáticos) no.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

