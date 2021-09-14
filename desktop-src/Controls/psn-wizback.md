---
title: PSN_WIZBACK de notificación (Prsht.h)
description: Notifica a una página que el usuario ha hecho clic en el botón Atrás en un asistente. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 784f92e7-6f10-40fc-b513-bea022f13ae1
keywords:
- PSN_WIZBACK código de notificación Windows controles
topic_type:
- apiref
api_name:
- PSN_WIZBACK
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed1cdd742d78473266db07899796de5a5450310
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167426"
---
# <a name="psn_wizback-notification-code"></a>Código de notificación \_ WIZBACK de PSN

Notifica a una página que el usuario ha hecho clic en el **botón** Atrás de un asistente. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_WIZBACK 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación. Esta estructura contiene una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **hdr**. El **miembro hwndFrom** de esta **estructura NMHDR** contiene el identificador de la hoja de propiedades. El **miembro lParam** de la **estructura PSHNOTIFY** no contiene ninguna información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 para permitir que el asistente vaya a la página anterior. Devuelve -1 para evitar que el asistente cambie de página. Para mostrar una página determinada, devuelva su identificador de recurso de cuadro de diálogo. Si el cuadro de diálogo se especificó con la [**marca \_ DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) de PSP, esta notificación devuelve el puntero a la plantilla de diálogo.

## <a name="remarks"></a>Observaciones

Para establecer el valor devuelto, el procedimiento del cuadro de diálogo de la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor **\_ MSGRESULT de DWL** y devolver **TRUE**. Por ejemplo:

``` syntax
case PSN_WIZBACK :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZNEXT :
    ...
```

> [!Note]  
> La hoja de propiedades está en proceso de manipular la lista de páginas cuando se envía el código de notificación \_ WIZBACK de PSN. Puede agregar, insertar o quitar páginas en respuesta a estos códigos de notificación, pero debe tener especial cuidado si inserta o quita páginas antes de la página actual.

 

Si inserta o quita páginas antes de la página actual, debe devolver (a través de **\_ MSGRESULT de DWL)** un valor distinto de cero para especificar la nueva página deseada. Sin embargo, tenga en cuenta que si inserta o quita una página que se encuentra antes de la página actual (que tiene un índice más pequeño que la página actual), [PSN \_ KILLACTIVE](psn-killactive.md) podría enviarse a la página incorrecta.

Por este motivo, se recomienda que los asistentes que agreguen y quiten páginas dinámicamente en respuesta a [ \_ PSN WIZNEXT](psn-wiznext.md) y \_ PSN WIZBACK solo lo hagan en las páginas al final de la lista. Si desea que el asistente quite las páginas con precisión, mantenga las páginas dinámicas al final de la lista y vuelva a las páginas permanentes antes de eliminarlas.

Por ejemplo, suponga que un asistente consta de una página de introducción, una serie de páginas dinámicas y una página de finalización, y desea eliminar las páginas dinámicas cuando el usuario llegue a la página de finalización.

1.  El asistente comenzaría con dos páginas, "Introducción" y "Finalización". El usuario comienza en la página "Introducción".
    1.  Introducción (el usuario está aquí)
    2.  Completion
2.  Cuando el usuario se aleja de "Introducción", el asistente agrega las páginas dinámicas y coloca al usuario en la primera página dinámica devolviendo (a través de **DWL \_ MSGRESULT)** el identificador de diálogo de la página "Dynamic 1". En este ejemplo, hay tres páginas dinámicas.
    1.  Introducción
    2.  Completion
    3.  Dinámica 1 (el usuario está aquí)
    4.  Dinámica 2
    5.  Dinámica 3
3.  Una vez que el usuario navega por las páginas dinámicas a "Dynamic 3" y, a continuación, navega a la página siguiente, la aplicación debe colocar al usuario en la página "Completion". De nuevo, esto se hace devolviendo (a través de **\_ MSGRESULT de DWL)** el identificador de cuadro de diálogo de la página "Completion".
    1.  Introducción
    2.  Finalización (el usuario está aquí)
    3.  Dinámica 1
    4.  Dinámica 2
    5.  Dinámica 3
4.  A continuación, la aplicación puede quitar las tres páginas dinámicas (numeradas de tres a cinco) de forma segura.
    1.  Introducción
    2.  Finalización (el usuario está aquí)

Tenga en cuenta que esta técnica solo es necesaria si el asistente quita páginas dinámicamente. Si el asistente solo agrega páginas dinámicamente, este proceso no es necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

