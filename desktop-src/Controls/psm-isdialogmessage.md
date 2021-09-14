---
title: PSM_ISDIALOGMESSAGE mensaje (Prsht.h)
description: Pasa un mensaje a un cuadro de diálogo de hoja de propiedades e indica si el cuadro de diálogo procesó el mensaje. Puede enviar este mensaje explícitamente o mediante la macro \_ PropSheet IsDialogMessage.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- PSM_ISDIALOGMESSAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b753fc849d76e3ac5071dd85bdd94950460fbb10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167541"
---
# <a name="psm_isdialogmessage-message"></a>Mensaje \_ ISDIALOGMESSAGE de PSM

Pasa un mensaje a un cuadro de diálogo de hoja de propiedades e indica si el cuadro de diálogo procesó el mensaje. Puede enviar este mensaje explícitamente o mediante la [**macro \_ PropSheet IsDialogMessage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura MSG**](/windows/win32/api/winuser/ns-winuser-msg) que contiene el mensaje que se va a comprobar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se ha procesado el mensaje o **FALSE** si el mensaje no se ha procesado.

## <a name="remarks"></a>Observaciones

El bucle de mensajes debe usar el mensaje **\_ ISDIALOGMESSAGE** de PSM con hojas de propiedades modeladas para pasar mensajes al cuadro de diálogo de hoja de propiedades. En los sistemas que admiten Unicode, use las versiones Unicode de las funciones [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) y [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) **(GetMessageW** y **PeekMessageW)** para recuperar mensajes.

Si el valor devuelto indica que se procesó el mensaje, no se debe pasar a la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) o [**DispatchMessage.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

