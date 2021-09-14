---
title: PSM_REMOVEPAGE mensaje (Prsht.h)
description: Quita una página de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro \_ RemovePage de PropSheet.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- PSM_REMOVEPAGE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167521"
---
# <a name="psm_removepage-message"></a>Mensaje \_ REMOVEPAGE de PSM

Quita una página de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro [**\_ RemovePage de PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la página que se va a quitar.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador HPROPSHEETPAGE de la página que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una aplicación puede especificar el índice o el identificador, o ambos. Si se especifican ambos, *lParam* tiene prioridad.

El **envío de PSM \_ REMOVEPAGE** destruye la página de la hoja de propiedades que se está quitando.

Se producen varios mensajes y una llamada de función mientras la hoja de propiedades manipula la lista de páginas. Mientras se realiza esta acción, el intento de modificar la lista de páginas tendrá resultados impredecibles. En consecuencia, no debe usar el mensaje **\_ REMOVEPAGE** de PSM en la implementación de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ni al controlar las siguientes notificaciones y Windows mensajes.

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

Puede agregar o quitar páginas en respuesta a estas notificaciones, siempre que devuelva (a través de MSGRESULT de DWL) un valor distinto de cero para especificar la \_ nueva página deseada. Sin embargo, tenga en cuenta que si quita una página que se encuentra antes de la página actual (que tiene un índice más pequeño que la página actual), [PSN \_ KILLACTIVE](psn-killactive.md) podría enviarse a la página incorrecta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

