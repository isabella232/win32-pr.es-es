---
title: Código de notificación de NM_RDBLCLK (barra de estado) (commctrl. h)
description: Notifica a las ventanas principales de un control de barra de estado que el usuario hizo doble clic con el botón secundario del mouse en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 57d8c5a7-e179-4b65-a3aa-5566d5780c18
keywords:
- Código de notificación de NM_RDBLCLK (barra de estado) controles de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493312"
---
# <a name="nm_rdblclk-status-bar-notification-code"></a>Código de notificación de NM \_ RDBLCLK (barra de estado)

Notifica a las ventanas principales de un control de barra de estado que el usuario hizo doble clic con el botón secundario del mouse en el control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_RDBLCLK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación. El miembro **dwItemSpec** contiene el índice de la sección en la que se hizo clic.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** para indicar que se controló el clic del mouse y suprime el procesamiento predeterminado por parte del sistema. Devuelve **false** para permitir el procesamiento predeterminado del clic.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





