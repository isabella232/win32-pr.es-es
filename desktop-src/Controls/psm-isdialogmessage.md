---
title: Mensaje de PSM_ISDIALOGMESSAGE (Prsht. h)
description: Pasa un mensaje a un cuadro de diálogo de hoja de propiedades e indica si el cuadro de diálogo procesó el mensaje. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ IsDialogMessage.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- PSM_ISDIALOGMESSAGE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905288"
---
# <a name="psm_isdialogmessage-message"></a>Mensaje de PSM \_ ISDIALOGMESSAGE

Pasa un mensaje a un cuadro de diálogo de hoja de propiedades e indica si el cuadro de diálogo procesó el mensaje. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) que contiene el mensaje que se va a comprobar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si se ha procesado el mensaje o **false** si el mensaje no se ha procesado.

## <a name="remarks"></a>Observaciones

El bucle de mensajes debería usar el mensaje **PSM \_ ISDIALOGMESSAGE** con hojas de propiedades no modales para pasar mensajes al cuadro de diálogo hoja de propiedades. En los sistemas que admiten Unicode, use las versiones Unicode de las funciones [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) y [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**GetMessageW** y **PeekMessageW**) para recuperar mensajes.

Si el valor devuelto indica que se procesó el mensaje, no se debe pasar a la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) o [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

