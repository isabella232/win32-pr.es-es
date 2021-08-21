---
title: PSN_QUERYINITIALFOCUS de notificación (Prsht.h)
description: Enviado por una hoja de propiedades para proporcionar una página de hoja de propiedades una oportunidad para especificar qué control de cuadro de diálogo debe recibir el foco inicial. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- PSN_QUERYINITIALFOCUS código de notificación Windows controles
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc82fe11893e728fbc9301868d9acdca5f7110bedfd37b4a16b473de0821f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169645"
---
# <a name="psn_queryinitialfocus-notification-code"></a>Código de \_ notificación PSN QUERYINITIALFOCUS

Enviado por una hoja de propiedades para proporcionar una página de hoja de propiedades una oportunidad para especificar qué control de cuadro de diálogo debe recibir el foco inicial. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PSHNOTIFY.**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) Convertir el **miembro lParam** de esta estructura en un tipo **HWND** para recuperar el identificador del control al que se le dará el foco de forma predeterminada. La estructura contiene una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **hdr**. El **miembro hwndFrom** de esta **estructura NMHDR** contiene el identificador de la hoja de propiedades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para especificar qué control debe recibir el foco, devuelva el identificador del control. De lo contrario, devuelva cero y el foco irá al control predeterminado. Para establecer el valor devuelto, el procedimiento del cuadro de diálogo debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con un valor **\_ MSGRESULT de DWL** y devolver **TRUE**.

## <a name="remarks"></a>Comentarios

Una aplicación no debe llamar a la [**función SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) mientras se administra este código de notificación. Devuelve el identificador del control que debe recibir el foco y el administrador de la hoja de propiedades controlará el cambio de foco.

El código de notificación PSN QUERYINITIALFOCUS no se envía si el administrador de la hoja de propiedades determina que ningún control de la página \_ debe recibir el foco.

Este fragmento de código implementa un controlador simple para PSN \_ QUERYINITIALFOCUS. Solicita que se le de foco inicial al control Ubicación (**IDC \_ LOCATION**).

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> Este código de notificación no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

