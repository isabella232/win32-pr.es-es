---
title: PSM_ISDIALOGMESSAGE mensaje (Prsht.h)
description: Pasa un mensaje a un cuadro de diálogo de hoja de propiedades e indica si el cuadro de diálogo procesó el mensaje. Puede enviar este mensaje explícitamente o mediante la \_ macro PropSheet IsDialogMessage.
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
ms.openlocfilehash: 12f28d63e5586d3b083282db4e029551ce4e61d0ef997e36e3e874e9f032095b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088685"
---
# <a name="psm_isdialogmessage-message"></a>Mensaje \_ ISDIALOGMESSAGE de PSM

Pasa un mensaje a un cuadro de diálogo de hoja de propiedades e indica si el cuadro de diálogo procesó el mensaje. Puede enviar este mensaje explícitamente o mediante la macro [**\_ PropSheet IsDialogMessage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage)

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

## <a name="remarks"></a>Comentarios

El bucle de mensajes debe usar el mensaje **\_ ISDIALOGMESSAGE** de PSM con hojas de propiedades modeless para pasar mensajes al cuadro de diálogo de hoja de propiedades. En los sistemas que admiten Unicode, use las versiones Unicode de las funciones [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) y [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) **(GetMessageW** y **PeekMessageW)** para recuperar mensajes.

Si el valor devuelto indica que se procesó el mensaje, no se debe pasar a la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) [**o DispatchMessage.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

