---
title: Mensaje de TDM_UPDATE_ICON (commctrl. h)
description: Actualiza el icono de un cuadro de diálogo de tarea.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- TDM_UPDATE_ICON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2da73ebb3bf0355f50bc08a08f0b35de97576b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997108"
---
# <a name="tdm_update_icon-message"></a>Mensaje de icono de \_ actualización de TDM \_

Actualiza el icono de un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Indica qué elemento de icono se va a actualizar. Este parámetro debe ser uno de los siguientes valores:



| Value                                                                                                                                                                   | Significado                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <dt>**icono de TDIE \_ \_ Main**</dt> </dl>       | Icono principal.<br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <dt>**TDIE \_ icono de \_ pie de página**</dt> </dl> | Icono de pie de página.<br/> |



 

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Un puntero a una cadena (PCWSTR) o un identificador a un icono (HICON) que se va a mostrar. Si *lParam* es **null**, no se muestra ningún icono, independientemente del valor de *wParam*.

Si el valor de *wParam* es TDIE \_ Icon \_ Main y la \_ marca TDF use \_ HICON \_ Main se establece en el miembro **dwFlags** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizada para crear el cuadro de diálogo de tarea, *lParam* debe contener un identificador de un icono (HICON) que se va a mostrar.

Si el valor de *wParam* es TDIE \_ Icon \_ footer y la marca TDF \_ use \_ HICON \_ footer está establecida en el miembro **dwFlags** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizada para crear el cuadro de diálogo de tarea, *lParam* debe contener un identificador de un icono (HICON) que se va a mostrar.

Si \_ \_ \_ no se establecen las marcas TDF HICON Main o TDF \_ use \_ HICON \_ de  pie de página en el miembro **dwFlags** , *lParam* debe apuntar a una cadena Unicode terminada en null (PCWSTR) que contiene un identificador de recurso válido que se pasa a través de la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) . El icono se muestra según el valor de *wParam*: Si el valor es TDIE \_ icono \_ Main, el icono se muestra en el encabezado; si el valor es TDIE \_ Icon \_ footer, el icono se muestra en el pie de página. El recurso debe ser del módulo de recursos de la aplicación (especificado en el miembro **hInstance** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) ) o si **hInstance** es **null**, del módulo de recursos del sistema (imageres.dll). Para identificar un recurso del sistema, use un identificador de sistema válido que se pase a través de la macro **MAKEINTRESOURCE** o uno de los siguientes valores predefinidos de commctrl. h:



| Value                                                                                                                                                                            | Significado                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <dt>**\_icono de error de TD \_**</dt> </dl>                   | Un icono de cierre de sesión.<br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <dt>**\_icono de advertencia de TD \_**</dt> </dl>             | Un icono de signo de exclamación.<br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <dt>**\_icono de información de TD \_**</dt> </dl> | Una letra minúscula "i" en un icono de círculo.<br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <dt>**icono de TD \_ Shield \_**</dt> </dl>                | Un icono de escudo de seguridad.<br/>                  |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Se puede producir un error en el diseño del cuadro de diálogo de tarea con el icono y es posible que no se refleje en el valor devuelto. Un valor devuelto de S \_ OK solo refleja que el cuadro de diálogo de tarea recibió el mensaje e intentó procesarlo. Si se produce un error en el diseño del cuadro de diálogo de tarea, el cuadro de diálogo se cerrará y se devolverá un código **HRESULT** en la función de devolución de llamada registrada. Para obtener más información sobre la sintaxis de la función de devolución de llamada, vea [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

Si el cuadro de diálogo de tarea se crea sin un pie de página (es decir, los miembros de pie de página correspondientes de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizada para crear el cuadro de diálogo de tarea son **null**) y se envía este mensaje, no se agrega de forma dinámica un pie de página al cuadro de diálogo de tarea. Lo mismo se aplica al enviar este mensaje para actualizar un icono de encabezado cuando se crea un cuadro de diálogo de tarea sin un encabezado. Para agregar un encabezado o un pie de página en tiempo de ejecución, use la funcionalidad de la [**\_ \_ Página de navegación de TDM**](tdm-navigate-page.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

