---
title: Código de notificación de PSN_RESET (Prsht. h)
description: Notifica a una página que la hoja de propiedades está a punto de ser destruida. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- PSN_RESET controles de código de notificación de Windows
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
ms.openlocfilehash: 5642a5354d934b37ee58007a9fb260befe201edd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656489"
---
# <a name="psn_reset-notification-code"></a>Código de notificación de restablecimiento de PSN \_

Notifica a una página que la hoja de propiedades está a punto de ser destruida. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Todos los cambios realizados desde el último código de notificación de [ \_ aplicación de PSN](psn-apply.md) se cancelan, excepto en el caso de [**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), que no admite ese código de notificación.

El miembro **lParam** de la estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) señalada por *lParam* se establecerá en **true** si el usuario hizo clic en el botón **X** situado en la esquina superior derecha de la hoja de propiedades. Será **false** si el usuario hizo clic en el botón **Cancelar** . La estructura **PSHNOTIFY** contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades.

Una aplicación puede utilizar este código de notificación como una oportunidad para realizar operaciones de limpieza.

> [!Note]  
> La hoja de propiedades está en proceso de manipular la lista de páginas cuando \_ se envía el código de notificación de restablecimiento de PSN. No intente agregar, quitar o insertar páginas mientras controla este código de notificación. Si lo hace, tendrá resultados imprevisibles.

 

No llame a la función [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) al procesar este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

