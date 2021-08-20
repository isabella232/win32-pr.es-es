---
title: PSM_ADDPAGE mensaje (Prsht.h)
description: Agrega una nueva página al final de una hoja de propiedades existente. Puede enviar este mensaje explícitamente o mediante la macro \_ PropSheet AddPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- PSM_ADDPAGE controles de Windows mensaje
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
ms.openlocfilehash: d17e9da965e5e45c6fe11bc319436c00663fdc6348d3d2457b3c15472f6f3868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169831"
---
# <a name="psm_addpage-message"></a>Mensaje \_ ADDPAGE de PSM

Agrega una nueva página al final de una hoja de propiedades existente. Puede enviar este mensaje explícitamente o mediante la [**macro \_ PropSheet AddPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la página que se agregará. La página debe haber sido creada por una llamada anterior a la [**función CreatePropertySheetPage.**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

La nueva página no debe ser mayor que la página más grande actualmente en la hoja de propiedades porque no se cambia el tamaño de la hoja de propiedades para ajustarse a la nueva página.

Se producen varios mensajes y una llamada de función mientras la hoja de propiedades manipula la lista de páginas. Mientras se realiza esta acción, el intento de modificar la lista de páginas tendrá resultados impredecibles. En consecuencia, no debe usar el mensaje ADDPAGE de PSM en la implementación de \_ [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ni mientras se administran las siguientes notificaciones y Windows mensajes.

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [RESTABLECIMIENTO DE \_ PSN](psn-reset.md)
-   [PSN \_ SETACTIVE](psn-setactive.md)
-   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

Si necesita modificar una página de hoja de propiedades mientras está controlando uno de estos mensajes o mientras [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) está en funcionamiento, publique un mensaje Windows privado. La aplicación no recibirá ese mensaje hasta que el administrador de la hoja de propiedades haya finalizado sus tareas. A continuación, puede modificar la lista de páginas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

