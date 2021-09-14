---
title: TDM_UPDATE_ICON mensaje (Commctrl.h)
description: Actualiza el icono de un cuadro de diálogo de tarea.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- TDM_UPDATE_ICON controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166102"
---
# <a name="tdm_update_icon-message"></a>Mensaje DE \_ ICONO DE ACTUALIZACIÓN DE TDM \_

Actualiza el icono de un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Indica qué elemento de icono se va a actualizar. Este parámetro debe ser uno de los siguientes valores:



| Value                                                                                                                                                                   | Significado                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <dt>**ICONO PRINCIPAL DE TDIE \_ \_**</dt> </dl>       | Icono principal.<br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <dt>**PIE DE PÁGINA DEL ICONO DE TDIE \_ \_**</dt> </dl> | Icono de pie de página.<br/> |



 

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una cadena (PCWSTR) o identificador a un icono (HICON) para mostrar. Si *lParam* es **NULL,** no se muestra ningún icono, independientemente del valor *de wParam*.

Si el valor de *wParam* es TDIE ICON MAIN y la marca TDF USE HICON MAIN está establecida en el miembro dwFlags de la estructura TASKDIALOGCONFIG utilizada para crear el cuadro de diálogo de tarea, lParam debe contener un identificador para mostrar \_ un icono \_ \_ \_ \_ (HICON).  [](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) 

Si el valor de *wParam* es TDIE ICON FOOTER y la marca TDF USE HICON FOOTER se establece en el miembro dwFlags de la estructura TASKDIALOGCONFIG utilizada para crear el cuadro de diálogo de tarea, lParam debe contener un identificador para mostrar \_ un icono \_ \_ \_ \_ (HICON).  [](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) 

Si las marcas USE HICON MAIN o TDF USE HICON FOOTER no están establecidas en el miembro \_ \_ \_ \_ \_ \_ **dwFlags,** *lParam*  [](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) debe apuntar a una cadena Unicode terminada en NULL (PCWSTR) que contenga un identificador de recurso válido pasado a través de la macro MAKEINTRESOURCE. El icono se muestra en función del valor de *wParam*: si el valor es TDIE ICON MAIN, el icono se muestra en el encabezado; si el valor es TDIE ICON FOOTER, el icono se muestra en el pie de \_ \_ \_ \_ página. El recurso debe ser del módulo de recursos de la aplicación (especificado en el **miembro hInstance** de la estructura [**TASKDIALOGCONFIG)**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) o si **hInstance** es **NULL,** del módulo de recursos del sistema (imageres.dll). Para identificar un recurso del sistema, use un identificador de sistema válido pasado a través de la macro **MAKEINTRESOURCE** o uno de los siguientes valores predefinidos de commctrl.h:



| Value                                                                                                                                                                            | Significado                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <dt>**ICONO DE ERROR DE TD \_ \_**</dt> </dl>                   | Icono de signo de detenerse.<br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <dt>**ICONO DE ADVERTENCIA DE TD \_ \_**</dt> </dl>             | Icono de signo de exclamación.<br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <dt>**ICONO DE INFORMACIÓN \_ DE \_ TD**</dt> </dl> | Una letra minúscula "i" en un icono de círculo.<br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <dt>**ICONO DE ESCUDO DE TD \_ \_**</dt> </dl>                | Icono de escudo de seguridad.<br/>                  |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

El diseño del cuadro de diálogo de tarea con el icono puede producir un error y es posible que esto no se refleje en el valor devuelto. Un valor devuelto de S OK refleja solo que el cuadro de diálogo de la tarea \_ recibió el mensaje e intentó procesarlo. Si se produce un error en el diseño del diálogo de tarea, el diálogo se cerrará y se devolverá un **código HRESULT** en la función de devolución de llamada registrada. Para obtener más información sobre la sintaxis de la función de devolución de llamada, vea [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

Si el cuadro de diálogo de tarea se crea sin un pie de página (es decir, los miembros de pie de página adecuados de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que se usa para crear el diálogo de tarea son **NULL)** y se envía este mensaje, no se agrega dinámicamente un pie de página al diálogo de tarea. Lo mismo sucede para enviar este mensaje para actualizar un icono de encabezado cuando se crea un cuadro de diálogo de tarea sin encabezado. Para agregar un encabezado o pie de página en tiempo de ejecución, use la funcionalidad [**\_ NAVIGATE PAGE \_ de TDM.**](tdm-navigate-page.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

