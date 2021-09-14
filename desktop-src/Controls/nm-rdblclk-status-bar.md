---
title: NM_RDBLCLK (barra de estado) código de notificación (Commctrl.h)
description: Notifica a las ventanas primarias de un control de barra de estado que el usuario ha hecho doble clic en el botón derecho del mouse dentro del control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 57d8c5a7-e179-4b65-a3aa-5566d5780c18
keywords:
- NM_RDBLCLK (barra de estado) código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18092b03a599c75a88deb56bb256d96728b96328
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167929"
---
# <a name="nm_rdblclk-status-bar-notification-code"></a>Código \_ de notificación DE NM RDBLCLK (barra de estado)

Notifica a las ventanas primarias de un control de barra de estado que el usuario ha hecho doble clic en el botón derecho del mouse dentro del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RDBLCLK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación. El **miembro dwItemSpec** contiene el índice de la sección en la que se hizo clic.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para indicar que el sistema controló el clic del mouse y suprime el procesamiento predeterminado. Devuelve **FALSE** para permitir el procesamiento predeterminado del clic.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





