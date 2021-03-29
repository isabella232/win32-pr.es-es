---
title: Mensaje de PSM_REMOVEPAGE (Prsht. h)
description: Quita una página de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ RemovePage.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- PSM_REMOVEPAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cae1611e1ed9540fce23d20681f44849903e5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905470"
---
# <a name="psm_removepage-message"></a>Mensaje de PSM \_ REMOVEPAGE

Quita una página de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la página que se va a quitar.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de HPROPSHEETPAGE de la página que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una aplicación puede especificar el índice o el identificador, o ambos. Si se especifican ambos, *lParam* tiene prioridad.

El envío de **PSM \_ REMOVEPAGE** destruye la página de la hoja de propiedades que se va a quitar.

Se producen varios mensajes y una llamada de función mientras la hoja de propiedades manipula la lista de páginas. Mientras se realiza esta acción, el intento de modificar la lista de páginas tendrá resultados imprevisibles. En consecuencia, no debe usar el mensaje **PSM \_ REMOVEPAGE** en la implementación de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) o mientras controla las siguientes notificaciones y mensajes de Windows.

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

Puede Agregar o quitar páginas en respuesta a estas notificaciones, siempre que devuelva (a través de DWL \_ MSGRESULT) un valor distinto de cero para especificar la nueva página deseada. Sin embargo, tenga en cuenta que si quita una página que se encuentra antes de la página actual (que tiene un índice más pequeño que la página actual), [PSN \_ KILLACTIVE](psn-killactive.md) podría enviarse a una página equivocada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

