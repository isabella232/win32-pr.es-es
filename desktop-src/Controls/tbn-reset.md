---
title: Código de notificación de TBN_RESET (commctrl. h)
description: Notifica a la ventana primaria de la barra de herramientas que el usuario ha restablecido el contenido del cuadro de diálogo Personalizar barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- TBN_RESET controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117ee2a50445ffe4dd8cd23d952fde7836bcf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079713"
---
# <a name="tbn_reset-notification-code"></a>Código de notificación de restablecimiento de TBN \_

Notifica a la ventana primaria de la barra de herramientas que el usuario ha restablecido el contenido del cuadro de diálogo Personalizar barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Vuelva TBNRF \_ ENDCUSTOMIZE para cerrar el cuadro de diálogo Personalizar barra de herramientas. Se omiten todos los demás valores devueltos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





