---
title: Código de notificación de PSN_WIZBACK (Prsht. h)
description: Notifica a una página que el usuario ha hecho clic en el botón atrás en un asistente. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 784f92e7-6f10-40fc-b513-bea022f13ae1
keywords:
- PSN_WIZBACK controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904989"
---
# <a name="psn_wizback-notification-code"></a>Código de notificación de WIZBACK de PSN \_

Notifica a una página que el usuario ha hecho clic en el botón **atrás** en un asistente. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
PSN_WIZBACK 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación. Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades. El miembro **lParam** de la estructura **PSHNOTIFY** no contiene ninguna información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 para permitir que el asistente vaya a la página anterior. Devuelve-1 para evitar que el asistente cambie las páginas. Para mostrar una página determinada, devuelva su identificador de recurso de cuadro de diálogo. Si el cuadro de diálogo se ha especificado con la marca [**PSP \_ DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) , esta notificación devuelve el puntero a la plantilla de cuadro de diálogo.

## <a name="remarks"></a>Observaciones

Para establecer el valor devuelto, el procedimiento de cuadro de diálogo de la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de **DWL \_ MSGRESULT** y devolver **true**. Por ejemplo:

``` syntax
case PSN_WIZBACK :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZNEXT :
    ...
```

> [!Note]  
> La hoja de propiedades está en proceso de manipular la lista de páginas cuando \_ se envía el código de notificación WIZBACK de PSN. Puede Agregar, insertar o quitar páginas en respuesta a estos códigos de notificación, pero debe tener cuidado especial si inserta o quita páginas antes de la página actual.

 

Si inserta o quita páginas antes de la página actual, debe devolver (a **DWL \_ MSGRESULT**) un valor distinto de cero para especificar la nueva página deseada. Tenga en cuenta, sin embargo, que si inserta o quita una página que se encuentra antes de la página actual (que tiene un índice más pequeño que la página actual), [PSN \_ KILLACTIVE](psn-killactive.md) podría enviarse a una página equivocada.

Por esta razón, se recomienda que los asistentes que agregan y quitan páginas dinámicamente en respuesta a [PSN \_ WIZNEXT](psn-wiznext.md) y PSN \_ WIZBACK lo hagan solo en las páginas al final de la lista. Si desea que el asistente Quite las páginas con precisión, mantenga las páginas dinámicas al final de la lista y vuelva a las páginas permanentes antes de eliminarlas.

Por ejemplo, supongamos que un asistente está formado por una página de introducción, una serie de páginas dinámicas y una página de finalización, y desea eliminar las páginas dinámicas cuando el usuario llega a la página de finalización.

1.  El asistente comenzaría con dos páginas: "introducción" y "finalización". El usuario comienza en la página "introducción".
    1.  Introducción (el usuario está aquí)
    2.  Completion
2.  Cuando el usuario sale de la "introducción", el asistente agrega las páginas dinámicas y coloca al usuario en la primera página dinámica devolviendo (a **DWL \_ MSGRESULT**) el identificador del cuadro de diálogo de la página "dinámica 1". En este ejemplo, hay tres páginas dinámicas.
    1.  Introducción
    2.  Completion
    3.  Dinámica 1 (el usuario está aquí)
    4.  Dinámica 2
    5.  Dinámica 3
3.  Una vez que el usuario navega por las páginas dinámicas a "Dynamic 3" y, a continuación, navega a la página siguiente, la aplicación debe poner al usuario en la página "completada". De nuevo, esto se hace devolviendo (hasta **DWL \_ MSGRESULT**) el identificador del cuadro de diálogo de la página "finalización".
    1.  Introducción
    2.  Finalización (el usuario está aquí)
    3.  Dinámica 1
    4.  Dinámica 2
    5.  Dinámica 3
4.  A continuación, la aplicación puede quitar las tres páginas dinámicas (numeradas de tres a cinco) sin ningún riesgo.
    1.  Introducción
    2.  Finalización (el usuario está aquí)

Tenga en cuenta que esta técnica solo es necesaria si el asistente quita las páginas dinámicamente. Si el asistente solo agrega páginas dinámicamente, este proceso no es necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

