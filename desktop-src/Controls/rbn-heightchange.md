---
title: Código de notificación de RBN_HEIGHTCHANGE (commctrl. h)
description: Se envía por un control Rebar cuando su alto ha cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: cf90e38c-ac3e-4bef-b047-0956ae5041d1
keywords:
- RBN_HEIGHTCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_HEIGHTCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe0601e8cb22ec9b86768741c5b455aa7f21eef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996330"
---
# <a name="rbn_heightchange-notification-code"></a>Código de notificación de HEIGHTCHANGE de RBN \_

Se envía por un control Rebar cuando su alto ha cambiado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
RBN_HEIGHTCHANGE

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para esta notificación.

## <a name="remarks"></a>Observaciones

Los controles Rebar que usan el estilo [**CCS \_ Vert**](common-control-styles.md) envían este código de notificación cuando cambia el ancho.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





