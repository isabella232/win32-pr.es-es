---
title: Código de notificación de LVN_MARQUEEBEGIN (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que ha empezado una selección de cuadro de límite (marquesina). Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- LVN_MARQUEEBEGIN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658416"
---
# <a name="lvn_marqueebegin-notification-code"></a>Código de notificación de MARQUEEBEGIN de LVN \_

Notifica a la ventana primaria de un control de vista de lista que ha empezado una selección de cuadro de límite (marquesina). Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para aceptar el código de notificación, devuelve cero. Para salir de la selección del cuadro de límite, devuelve un valor distinto de cero.

## <a name="remarks"></a>Observaciones

Una *selección de cuadro de límite* es el proceso de hacer clic en el área cliente de la ventana de vista de lista y arrastrar para seleccionar varios elementos simultáneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





