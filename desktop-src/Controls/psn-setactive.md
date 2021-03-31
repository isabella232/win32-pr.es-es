---
title: Código de notificación de PSN_SETACTIVE (Prsht. h)
description: Notifica a una página que está a punto de activarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- PSN_SETACTIVE controles de código de notificación de Windows
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
ms.openlocfilehash: 1f38db77c1c60ef60ce713d41a6112b42235b79a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996640"
---
# <a name="psn_setactive-notification-code"></a>Código de notificación de SETACTIVE de PSN \_

Notifica a una página que está a punto de activarse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación. Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades. El miembro **lParam** de la estructura **PSHNOTIFY** no contiene ninguna información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para aceptar la activación, o-1 para activar la página siguiente o anterior (en función de si el usuario hizo clic en el botón **siguiente** o **atrás** ). Para establecer la activación en una página determinada, devuelva el identificador de recursos de la página.

## <a name="remarks"></a>Observaciones

El \_ código de notificación SETACTIVE de PSN se envía antes de que la página esté visible. Una aplicación puede utilizar este código de notificación para inicializar los datos en la página.

> [!Note]  
> La hoja de propiedades está en proceso de manipular la lista de páginas cuando \_ se envía el código de notificación SETACTIVE de PSN. No intente agregar, quitar o insertar páginas mientras controla este código de notificación. Si lo hace, tendrá resultados imprevisibles.

 

Para establecer el valor devuelto, el procedimiento de cuadro de diálogo de la página debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de DWL \_ MSGRESULT y el procedimiento de cuadro de diálogo debe devolver **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

