---
title: PSN_SETACTIVE de notificación (Prsht.h)
description: Notifica a una página que está a punto de activarse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- PSN_SETACTIVE código de notificación Windows controles
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e7b656f5497065378af87408fa87fc16cf9ca2cef3cc710f52a1cd643c2927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409737"
---
# <a name="psn_setactive-notification-code"></a>Código de notificación SETACTIVE de PSN \_

Notifica a una página que está a punto de activarse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación. Esta estructura contiene una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **hdr**. El **miembro hwndFrom** de esta **estructura NMHDR** contiene el identificador de la hoja de propiedades. El **miembro lParam** de la **estructura PSHNOTIFY** no contiene ninguna información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para aceptar la activación o -1 para activar la página siguiente o anterior (en función de si el usuario hizo clic en el botón **Siguiente** **o** Atrás). Para establecer la activación en una página determinada, devuelva el identificador de recurso de la página.

## <a name="remarks"></a>Comentarios

El código de notificación SETACTIVE de PSN \_ se envía antes de que la página esté visible. Una aplicación puede usar este código de notificación para inicializar datos en la página.

> [!Note]  
> La hoja de propiedades está en proceso de manipular la lista de páginas cuando se envía el código de notificación \_ SETACTIVE de PSN. No intente agregar, quitar ni insertar páginas mientras administra este código de notificación. Si lo hace, tendrá resultados impredecibles.

 

Para establecer el valor devuelto, el procedimiento del cuadro de diálogo de la página debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor MSGRESULT de DWL y el procedimiento del cuadro de diálogo debe \_ devolver **TRUE**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

