---
title: TDM_NAVIGATE_PAGE mensaje (Commctrl.h)
description: Vuelve a crear un cuadro de diálogo de tarea con contenido nuevo, simulando la funcionalidad de un asistente para varias páginas.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- TDM_NAVIGATE_PAGE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166133"
---
# <a name="tdm_navigate_page-message"></a>Mensaje DE \_ LA PÁGINA DE NAVEGACIÓN de TDM \_

Vuelve a crear un cuadro de diálogo de tarea con contenido nuevo, simulando la funcionalidad de un asistente para varias páginas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

No se usa. Debe ser cero.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una [**estructura TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que describe el cuadro de diálogo de tarea que se creará. La aplicación que realiza la llamada debe asignar esta estructura y establecer sus miembros. Los valores de los miembros varían según el tipo de página a la que vaya el usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Para iniciar un cuadro de diálogo de tarea del asistente, use [**la función TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) A medida que el usuario navega mediante el asistente, envíe este mensaje al cuadro de diálogo de tarea para mostrar la página siguiente. Se crea un nuevo cuadro de diálogo de tarea (parece una nueva página) con los elementos especificados en la estructura a la que *apunta lParam*. Durante la creación, se destruye y se reconstruye todo el contenido del marco de diálogo. Como resultado, se pierde cualquier información de estado que mantienen los controles (por ejemplo, una barra de progreso, un botón expando o una casilla de verificación) en el cuadro de diálogo.

El diseño del cuadro de diálogo de tarea puede producir un error y es posible que esto no se refleje en el valor devuelto. Un valor devuelto de S OK refleja solo que el cuadro de \_ diálogo de tarea recibió el mensaje e intentó procesarlo. Si se produce un error en el diseño del diálogo de tarea (no se puede mostrar el cuadro de diálogo de tarea), el diálogo se cerrará y se devolverá un **código HRESULT** en la función de devolución de llamada registrada. Para obtener más información sobre la sintaxis de la función de devolución de llamada, vea [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

