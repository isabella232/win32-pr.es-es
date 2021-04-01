---
title: Código de notificación de PSN_QUERYINITIALFOCUS (Prsht. h)
description: Enviado por una hoja de propiedades para proporcionar a la página de la hoja de propiedades una oportunidad para especificar qué control de cuadro de diálogo debe recibir el foco inicial. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- PSN_QUERYINITIALFOCUS controles de código de notificación de Windows
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
ms.openlocfilehash: bc542332440009f6564f384b415657e725edda00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149940"
---
# <a name="psn_queryinitialfocus-notification-code"></a>Código de notificación de QUERYINITIALFOCUS de PSN \_

Enviado por una hoja de propiedades para proporcionar a la página de la hoja de propiedades una oportunidad para especificar qué control de cuadro de diálogo debe recibir el foco inicial. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) . Convierta el miembro **lParam** de esta estructura a un tipo **hWnd** para recuperar el identificador del control al que se asignará el foco de forma predeterminada. La estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para especificar el control que debe recibir el foco, devuelva el identificador del control. De lo contrario, devuelve cero y Focus irá al control predeterminado. Para establecer el valor devuelto, el procedimiento del cuadro de diálogo debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con un valor de **DWL \_ MSGRESULT** y devolver **true**.

## <a name="remarks"></a>Observaciones

Una aplicación no debe llamar a la función [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) mientras controla este código de notificación. Devuelve el identificador del control que debe recibir el foco y el administrador de la hoja de propiedades controlará el cambio de foco.

\_No se envía el código de notificación PSN QUERYINITIALFOCUS si el administrador de la hoja de propiedades determina que ningún control de la página debe recibir el foco.

Este fragmento de código implementa un controlador simple para PSN \_ QUERYINITIALFOCUS. Solicita que se proporcione el foco inicial al control de ubicación (**\_ Ubicación de IDC**).

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> Este código de notificación no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

