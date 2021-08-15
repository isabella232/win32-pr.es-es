---
title: PSN_RESET de notificación (Prsht.h)
description: Notifica a una página que la hoja de propiedades está a punto de destruirse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- PSN_RESET código de notificación Windows controles
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb9f14b037d8757469497e644d870a887e6db36172b171f31b00d5615ff39532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409816"
---
# <a name="psn_reset-notification-code"></a>Código de notificación \_ de PSN RESET

Notifica a una página que la hoja de propiedades está a punto de destruirse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Todos los cambios realizados desde el último código de [notificación DE PSN \_ APPLY](psn-apply.md) se cancelan, excepto en el caso de [**PSH \_ AEROWIZARD,**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)que no admite ese código de notificación.

El **miembro lParam** de la estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) a la que *apunta lParam* se establecerá en **TRUE** si el usuario hizo clic en el botón **X** de la esquina superior derecha de la hoja de propiedades. Será FALSE **si el** usuario hizo clic en el **botón** Cancelar. La **estructura PSHNOTIFY** contiene una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **hdr.** El **miembro hwndFrom** de esta **estructura NMHDR** contiene el identificador de la hoja de propiedades.

Una aplicación puede usar este código de notificación como una oportunidad para realizar operaciones de limpieza.

> [!Note]  
> La hoja de propiedades está en proceso de manipular la lista de páginas cuando se envía el código de notificación \_ de PSN RESET. No intente agregar, quitar ni insertar páginas mientras administra este código de notificación. Si lo hace, tendrá resultados impredecibles.

 

No llame a la [**función EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) al procesar este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

