---
title: Código de notificación de LVN_GETINFOTIP (commctrl. h)
description: Se envía mediante una vista de iconos grandes control de vista de lista que tiene el \_ estilo extendido LVS ex previsor \_ .
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535644"
---
# <a name="lvn_getinfotip-notification-code"></a>Código de notificación de GETINFOTIP de LVN \_

Se envía mediante una vista de iconos grandes control de vista de lista que tiene el estilo extendido [**LVS \_ ex \_**](extended-list-view-styles.md) previsor. Este código de notificación se envía cuando el control de vista de lista solicita información de texto adicional que se va a mostrar en una información sobre herramientas. Se envía en forma de un mensaje de [**\_ notificación de WM**](wm-notify.md) .


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) que contiene información sobre este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para esta notificación.

## <a name="remarks"></a>Observaciones

Este código de notificación solo lo envían los controles de vista de lista que tienen el estilo extendido [**LVS \_ ex \_**](extended-list-view-styles.md) previsor. El \_ código de notificación LVN GETINFOTIP se envía solo para el subelemento 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVN \_ GETINFOTIPW** (Unicode) y **LVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





