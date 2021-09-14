---
title: PSM_INSERTPAGE mensaje (Prsht.h)
description: Inserta una nueva página en una hoja de propiedades existente. La página se puede insertar en un índice especificado o después de una página especificada. Puede enviar este mensaje explícitamente o mediante la macro \_ PropSheet InsertPage.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- PSM_INSERTPAGE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167557"
---
# <a name="psm_insertpage-message"></a>Mensaje \_ INSERTPAGE de PSM

Inserta una nueva página en una hoja de propiedades existente. La página se puede insertar en un índice especificado o después de una página especificada. Puede enviar este mensaje explícitamente o mediante la [**macro \_ PropSheet InsertPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Donde se va a insertar la página. Establezca este parámetro en **NULL** para convertir la nueva página en la primera página. Para especificar dónde se va a insertar la nueva página, puede pasar un índice o el identificador HPROPSHEETPAGE de una página existente.



| Value                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt> <dt>index</dt> </dl>            | Si el *parámetro wParam* es menor que MAXUSHORT (el entero corto sin signo más grande), *wParam* especifica el índice de base cero para la nueva página. Por ejemplo, para convertir la página insertada en la tercera página de la hoja de propiedades, establezca *wParam* en 2. Para convertirla en la primera página, *establezca wParam* en 0. Si *wParam tiene* un valor mayor que el número de páginas y menor que MAXUSHORT, se anexará la página.<br/> |
| <dl> <dt></dt><dt>hpageInsertAfter</dt> </dl> | Si establece el *parámetro wParam* en el identificador HPROPSHEETPAGE de una página existente, la nueva página se insertará después.<br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la página que se va a insertar. La página debe crearse primero mediante una llamada a la [**función CreatePropertySheetPage.**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si la página se insertó correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

Las páginas después del punto de inserción se desplazan a la derecha para dar cabida a la nueva página.

No se cambia el tamaño de la hoja de propiedades para que se ajuste a la nueva página. No haga que la nueva página sea mayor que la página más grande de la hoja de propiedades.

Se producen varios mensajes y una llamada de función mientras la hoja de propiedades manipula la lista de páginas. Mientras se realiza esta acción, el intento de modificar la lista de páginas tendrá resultados impredecibles. En consecuencia, no debe usar el mensaje INSERTPAGE de PSM en la implementación de \_ [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ni mientras se administran las siguientes notificaciones y Windows mensajes.

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [RESTABLECIMIENTO DE \_ PSN](psn-reset.md)
-   [PSN \_ SETACTIVE](psn-setactive.md)
-   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

Si necesita modificar una página de hoja de propiedades mientras está controlando uno de estos mensajes o mientras [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) está en funcionamiento, publique un mensaje Windows privado. La aplicación no recibirá ese mensaje hasta que el administrador de la hoja de propiedades haya finalizado sus tareas. A continuación, puede modificar la lista de páginas.

Las siguientes notificaciones también se ven afectadas por la modificación de la hoja de propiedades.

-   [PSN \_ WIZBACK](psn-wizback.md)
-   [PSN \_ WIZNEXT](psn-wiznext.md)

Puede agregar o quitar páginas en respuesta a estas notificaciones, siempre que devuelva (a través de MSGRESULT de DWL) un valor distinto de cero para especificar la \_ nueva página deseada. Sin embargo, tenga en cuenta que si inserta una página que se encuentra antes de la página actual (que tiene un índice más pequeño que la página actual), [PSN \_ KILLACTIVE](psn-killactive.md) podría enviarse a la página incorrecta.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

