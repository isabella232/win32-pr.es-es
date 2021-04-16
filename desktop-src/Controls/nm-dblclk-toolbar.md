---
title: Código de notificación de NM_DBLCLK (barra de herramientas) (commctrl. h)
description: Notifica a la ventana primaria de un control de barra de herramientas que el usuario ha hace doble clic en el botón primario del mouse dentro del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: c6198245-cfd4-4e1f-877d-94c1d47e09d2
keywords:
- Código de notificación de NM_DBLCLK (barra de herramientas) controles de Windows
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5441f86fa47f25a98dad82f9bfde05a84b5f498
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489046"
---
# <a name="nm_dblclk-toolbar-notification-code"></a>NM \_ DBLCLK (barra de herramientas) código de notificación

Notifica a la ventana primaria de un control de barra de herramientas que el usuario ha hace doble clic en el botón primario del mouse dentro del control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_DBLCLK

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información sobre este código de notificación. Si se hizo clic con el mouse en un elemento de la barra de herramientas, el miembro **dwItemSpec** contiene el identificador del elemento y el miembro **dwItemData** contiene los datos del elemento. Si se hizo clic con el mouse en un separador o en un espacio en blanco en la barra de herramientas, el miembro **dwItemSpec** contendrá-1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **false** para permitir que el control de barra de herramientas realice el procesamiento predeterminado del evento, o bien **true** para evitar que el control procese el evento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





