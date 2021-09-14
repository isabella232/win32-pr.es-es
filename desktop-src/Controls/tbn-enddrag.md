---
title: TBN_ENDDRAG de notificación (Commctrl.h)
description: Notifica a la ventana primaria de la barra de herramientas que el usuario ha dejado de arrastrar un botón en una barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 846ba42e-6e0d-45bb-88ce-7b4d2cb17e13
keywords:
- TBN_ENDDRAG código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd493ac338e11716ea381e83102b200334a1eec4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166362"
---
# <a name="tbn_enddrag-notification-code"></a>Código de notificación \_ ENDDRAG de TBN

Notifica a la ventana primaria de la barra de herramientas que el usuario ha dejado de arrastrar un botón en una barra de herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_ENDDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTOOLBAR.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) El **miembro iItem** contiene el identificador de comando del botón que se está arrastrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





