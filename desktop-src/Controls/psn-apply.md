---
title: PSN_APPLY de notificación (Prsht.h)
description: Se envía a todas las páginas de la hoja de propiedades para indicar que el usuario ha hecho clic en el botón Aceptar, Cerrar o Aplicar y desea que todos los cambios suban efecto. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- PSN_APPLY código de notificación Windows controles
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167458"
---
# <a name="psn_apply-notification-code"></a>Código de notificación APPLY de PSN \_

Se envía a todas las páginas de la hoja de propiedades para indicar que el usuario ha hecho clic en el botón Aceptar, Cerrar o Aplicar y desea que todos los cambios suban efecto. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación, incluido el identificador de la página.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Establezca PSNRET NOERROR para indicar que los cambios realizados en esta página son válidos \_ y se han aplicado. Si todas las páginas establecen PSNRET \_ NOERROR, se puede destruir la hoja de propiedades. Para indicar que los cambios realizados en esta página no son válidos y para evitar que se destruya la hoja de propiedades, establezca uno de los siguientes valores devueltos:

-   PSNRET \_ NO ES VÁLIDO. La hoja de propiedades no se destruirá y el foco se devolverá a esta página.
-   PSNRET \_ INVALID \_ NOCHANGEPAGE. La hoja de propiedades no se destruirá y el foco se devolverá a la página que tenía el foco cuando se presionó el botón.

Para establecer el valor devuelto, el procedimiento del cuadro de diálogo de la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor MSGRESULT de DWL y el procedimiento del cuadro de diálogo debe \_ devolver **TRUE**.

## <a name="remarks"></a>Observaciones

Cuando el usuario hace clic en los botones Aceptar, Aplicar o Cerrar, la hoja de propiedades envía una notificación [ \_ KILLACTIVE](psn-killactive.md) de PSN a la página activa, lo que le ofrece la oportunidad de validar los cambios del usuario. Si los cambios son válidos, la hoja de propiedades envía un código de notificación APPLY de PSN a cada página, lo que le dirige para aplicar las nuevas propiedades \_ al elemento correspondiente.

> [!Note]  
> La hoja de propiedades está en proceso de manipular la lista de páginas cuando se envía el código de notificación \_ DE PSN APPLY. No intente agregar, quitar ni insertar páginas mientras se administra esta notificación. Si lo hace, tendrá resultados impredecibles.

 

El **miembro lParam** de la estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) a la que *apunta lParam* se establece en **TRUE** si el usuario hace clic en el botón Aceptar. También se establece en **TRUE si** se ha enviado el mensaje [**\_ CANCELTOCLOSE**](psm-canceltoclose.md) de PSM y el usuario hace clic en el botón Cerrar. Se establece en **FALSE si** el usuario hace clic en el botón Aplicar.

La [**estructura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contiene una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **hdr**. El **miembro hwndFrom** de esta **estructura NMHDR** contiene el identificador de la hoja de propiedades.

No llame a la [**función EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) al procesar este código de notificación.

Se destruye una hoja de propiedades modal si el usuario hace clic en el botón Aceptar y cada página devuelve el valor PSNRET NOERROR en respuesta \_ a **PSN \_ APPLY.** Si alguna página devuelve PSNRET \_ INVALID o PSNRET \_ INVALID \_ NOCHANGEPAGE, el proceso Aplicar se cancela inmediatamente. Las páginas después de la página de cancelación no recibirán un código de notificación \_ DE PSN APPLY.

Para recibir este código de notificación, una página debe establecer el valor MSGRESULT de DWL en FALSE en respuesta al código \_ [de notificación \_ KILLACTIVE de PSN.](psn-killactive.md) 

> [!Note]  
> Este código de notificación no se admite cuando se usa el estilo del asistente de Aero [**(PSH \_ AEROWIZARD).**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

