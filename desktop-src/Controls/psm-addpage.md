---
title: Mensaje de PSM_ADDPAGE (Prsht. h)
description: Agrega una nueva página al final de una hoja de propiedades existente. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ addPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- PSM_ADDPAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d09e07dfa2be86e11fa33863f091732955714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905473"
---
# <a name="psm_addpage-message"></a>Mensaje de PSM de PSM \_

Agrega una nueva página al final de una hoja de propiedades existente. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ addPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la página que se va a agregar. La página debe haber sido creada por una llamada anterior a la función [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

La nueva página no debe ser mayor que la página más grande que se encuentra actualmente en la hoja de propiedades porque no se cambia el tamaño de la hoja de propiedades para ajustarse a la nueva página.

Se producen varios mensajes y una llamada de función mientras la hoja de propiedades manipula la lista de páginas. Mientras se realiza esta acción, el intento de modificar la lista de páginas tendrá resultados imprevisibles. Por lo tanto, no debe usar el \_ mensaje de PSM en la implementación de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o mientras controla las siguientes notificaciones y mensajes de Windows.

-   [PSN \_ aplicar](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [restablecimiento de PSN \_](psn-reset.md)
-   [PSN \_ SETACTIVE](psn-setactive.md)
-   [**destrucción de WM \_**](/windows/desktop/winmsg/wm-destroy)
-   [**INITDIALOG de WM \_**](/windows/desktop/dlgbox/wm-initdialog)

Si tiene que modificar una página de la hoja de propiedades mientras está controlando uno de estos mensajes o mientras [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) está en funcionamiento, envíese a sí mismo un mensaje de Windows privado. La aplicación no recibirá ese mensaje hasta que el administrador de la hoja de propiedades haya finalizado sus tareas. A continuación, puede modificar la lista de páginas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

