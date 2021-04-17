---
title: Código de notificación de TBN_INITCUSTOMIZE (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que se ha iniciado la personalización. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- TBN_INITCUSTOMIZE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656463"
---
# <a name="tbn_initcustomize-notification-code"></a>Código de notificación de INITCUSTOMIZE de TBN \_

Notifica a la ventana primaria de una barra de herramientas que se ha iniciado la personalización. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) de la barra de herramientas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve TBNRF \_ HIDEHELP para suprimir el botón ayuda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





