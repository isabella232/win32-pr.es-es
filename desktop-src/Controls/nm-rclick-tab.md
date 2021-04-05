---
title: Código de notificación de NM_RCLICK (pestaña) (commctrl. h)
description: Notifica a la ventana primaria de un control de pestaña que el usuario ha hace clic con el botón secundario del mouse en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ef2270c0-eef3-4867-8aa3-b6ff7e1a5f0f
keywords:
- Controles de Windows de código de notificación de NM_RCLICK (pestaña)
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c74249e2c2984dd11dab7c4eab8147cb572f291
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079782"
---
# <a name="nm_rclick-tab-notification-code"></a>\_RCLICK código de notificación de nm (pestaña)

Notifica a la ventana primaria de un control de pestaña que el usuario ha hace clic con el botón secundario del mouse en el control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_RCLICK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero para no permitir el procesamiento predeterminado, o cero para permitir el procesamiento predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





