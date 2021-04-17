---
title: Mensaje de PSM_INSERTPAGE (Prsht. h)
description: Inserta una nueva página en una hoja de propiedades existente. La página puede insertarse en un índice especificado o después de una página especificada. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ InsertPage.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- PSM_INSERTPAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afdd58536a5cdd18d39a331df4b18c9bbae93842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658234"
---
# <a name="psm_insertpage-message"></a>Mensaje de PSM \_ INSERTPAGE

Inserta una nueva página en una hoja de propiedades existente. La página puede insertarse en un índice especificado o después de una página especificada. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Donde se va a insertar la página. Establezca este parámetro en **null** para que la nueva página sea la primera página. Para especificar dónde se va a insertar la nueva página, puede pasar un índice o el identificador HPROPSHEETPAGE de una página existente.



| Value                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt> <dt>index</dt> </dl>            | Si el parámetro *wParam* es menor que MAXUSHORT (el entero corto sin signo más grande), *wParam* especifica el índice de base cero para la nueva página. Por ejemplo, para convertir la página insertada en la tercera página de la hoja de propiedades, establezca *wParam* en 2. Para convertirlo en la primera página, establezca *wParam* en 0. Si *wParam* tiene un valor mayor que el número de páginas y menor que MAXUSHORT, se anexará la página.<br/> |
| <dl> <dt></dt><dt>hpageInsertAfter</dt> </dl> | Si establece el parámetro *wParam* en el identificador de HPROPSHEETPAGE de una página existente, la nueva página se insertará después.<br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la página que se va a insertar. La página debe crearse primero mediante una llamada a la función [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si la página se insertó correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

Las páginas después del punto de inserción se desplazan hacia la derecha para dar cabida a la nueva página.

No se cambia el tamaño de la hoja de propiedades para ajustarse a la nueva página. No haga que la nueva página sea más grande que la página más grande de la hoja de propiedades.

Se producen varios mensajes y una llamada de función mientras la hoja de propiedades manipula la lista de páginas. Mientras se realiza esta acción, el intento de modificar la lista de páginas tendrá resultados imprevisibles. En consecuencia, no debe usar el \_ mensaje PSM INSERTPAGE en la implementación de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o mientras controla las siguientes notificaciones y mensajes de Windows.

-   [PSN \_ aplicar](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [restablecimiento de PSN \_](psn-reset.md)
-   [PSN \_ SETACTIVE](psn-setactive.md)
-   [**destrucción de WM \_**](/windows/desktop/winmsg/wm-destroy)
-   [**INITDIALOG de WM \_**](/windows/desktop/dlgbox/wm-initdialog)

Si tiene que modificar una página de la hoja de propiedades mientras está controlando uno de estos mensajes o mientras [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) está en funcionamiento, envíese a sí mismo un mensaje de Windows privado. La aplicación no recibirá ese mensaje hasta que el administrador de la hoja de propiedades haya finalizado sus tareas. A continuación, puede modificar la lista de páginas.

Las siguientes notificaciones también se ven afectadas por la modificación de la hoja de propiedades.

-   [PSN \_ WIZBACK](psn-wizback.md)
-   [PSN \_ WIZNEXT](psn-wiznext.md)

Puede Agregar o quitar páginas en respuesta a estas notificaciones, siempre que devuelva (a través de DWL \_ MSGRESULT) un valor distinto de cero para especificar la nueva página deseada. Tenga en cuenta, sin embargo, que si inserta una página que se encuentra antes de la página actual (que tiene un índice menor que la página actual), [PSN \_ KILLACTIVE](psn-killactive.md) podría enviarse a una página equivocada.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

