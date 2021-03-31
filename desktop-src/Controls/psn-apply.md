---
title: Código de notificación de PSN_APPLY (Prsht. h)
description: Se envía a todas las páginas de la hoja de propiedades para indicar que el usuario ha hecho clic en el botón Aceptar, cerrar o aplicar y desea que todos los cambios surtan efecto. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- PSN_APPLY controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d8206b4e423fb01be3277a9dd0ca3a49b59129
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491440"
---
# <a name="psn_apply-notification-code"></a>PSN \_ aplicar código de notificación

Se envía a todas las páginas de la hoja de propiedades para indicar que el usuario ha hecho clic en el botón Aceptar, cerrar o aplicar y desea que todos los cambios surtan efecto. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación, incluido el identificador de la página.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Establezca PSNRET \_ NoError para indicar que los cambios realizados en esta página son válidos y se han aplicado. Si todas las páginas establecen PSNRET \_ NoError, se puede destruir la hoja de propiedades. Para indicar que los cambios realizados en esta página no son válidos y para evitar que se destruya la hoja de propiedades, establezca uno de los siguientes valores devueltos:

-   PSNRET \_ no válido. La hoja de propiedades no se destruirá y se devolverá el foco a esta página.
-   PSNRET \_ NOCHANGEPAGE no válido \_ . La hoja de propiedades no se destruirá y el foco se devolverá a la página que tenía el foco cuando se presionó el botón.

Para establecer el valor devuelto, el procedimiento de cuadro de diálogo de la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de DWL \_ MSGRESULT y el procedimiento de cuadro de diálogo debe devolver **true**.

## <a name="remarks"></a>Observaciones

Cuando el usuario hace clic en el botón Aceptar, aplicar o cerrar, la hoja de propiedades envía una notificación de [PSN \_ KILLACTIVE](psn-killactive.md) a la página activa, lo que le permite validar los cambios del usuario. Si los cambios son válidos, la hoja de propiedades envía un PSN \_ aplicar código de notificación a cada página y le dirige para aplicar las nuevas propiedades al elemento correspondiente.

> [!Note]  
> La hoja de propiedades está en proceso de manipular la lista de páginas cuando \_ se envía el código de notificación PSN. No intente agregar, quitar o insertar páginas mientras controla esta notificación. Si lo hace, tendrá resultados imprevisibles.

 

El miembro **lParam** de la estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) señalada por *lParam* se establece en **true** si el usuario hace clic en el botón Aceptar. También se establece en **true** si se ha enviado el mensaje de [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md) y el usuario hace clic en el botón Cerrar. Se establece en **false** si el usuario hace clic en el botón aplicar.

La estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades.

No llame a la función [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) al procesar este código de notificación.

Se destruye una hoja de propiedades modal si el usuario hace clic en el botón Aceptar y todas las páginas devuelven el \_ valor PSNRET NoError en respuesta a **PSN \_ Apply**. Si cualquier página devuelve PSNRET no \_ válido o PSNRET \_ NOCHANGEPAGE no válido \_ , el proceso de aplicación se cancela inmediatamente. Páginas después de la cancelación de la página no recibirá un código de notificación de aplicación de PSN \_ .

Para recibir este código de notificación, una página debe establecer el \_ valor de DWL MSGRESULT en **false** en respuesta al código de notificación de [PSN \_ KILLACTIVE](psn-killactive.md) .

> [!Note]  
> Este código de notificación no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

