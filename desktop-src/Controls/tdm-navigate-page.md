---
title: Mensaje de TDM_NAVIGATE_PAGE (commctrl. h)
description: Vuelve a crear un cuadro de diálogo de tarea con contenido nuevo, simulando la funcionalidad de un asistente de varias páginas.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- TDM_NAVIGATE_PAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56fc86e0e4fe457a43e035ed5d568e91303c7fcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997021"
---
# <a name="tdm_navigate_page-message"></a>Mensaje de página de \_ navegación de TDM \_

Vuelve a crear un cuadro de diálogo de tarea con contenido nuevo, simulando la funcionalidad de un asistente de varias páginas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

No se utiliza. Debe ser cero.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Puntero a una estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que describe el cuadro de diálogo de tarea que se va a crear. La aplicación que realiza la llamada debe asignar esta estructura y establecer sus miembros. Los valores de los miembros varían en función del tipo de página al que navega el usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Para iniciar un cuadro de diálogo de tarea del asistente, use la función [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Cuando el usuario navega con el asistente, envía este mensaje al cuadro de diálogo de la tarea para mostrar la página siguiente. Se crea un nuevo cuadro de diálogo de tarea (se parece a una nueva página) con los elementos especificados en la estructura a la que apunta *lParam*. En el momento de la creación, se destruye y se reconstruye todo el contenido del marco del cuadro de diálogo. Como resultado, se pierde toda la información de estado mantenida por los controles (por ejemplo, una barra de progreso, un botón Expando o una casilla de verificación) en el cuadro de diálogo.

Se puede producir un error en el diseño del cuadro de diálogo de tarea y es posible que no se refleje en el valor devuelto. Un valor devuelto de S \_ OK solo refleja que el cuadro de diálogo de tarea recibió el mensaje e intentó procesarlo. Si se produce un error en el diseño del cuadro de diálogo de tarea (no se puede mostrar el cuadro de diálogo de tarea), el cuadro de diálogo se cerrará y se devolverá un código **HRESULT** en la función de devolución de llamada registrada. Para obtener más información sobre la sintaxis de la función de devolución de llamada, vea [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

