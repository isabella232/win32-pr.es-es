---
title: Código de notificación de PGN_CALCSIZE (commctrl. h)
description: Lo envía un control de paginación para obtener las dimensiones desplazables de la ventana contenida.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- PGN_CALCSIZE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee6de1c45402f8bdc154f9f10be00140d7c766c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802065"
---
# <a name="pgn_calcsize-notification-code"></a>Código de notificación de CALCSIZE de PGN \_

Lo envía un control de paginación para obtener las dimensiones desplazables de la ventana contenida. El control de paginación utiliza estas dimensiones para determinar el tamaño desplazable de la ventana contenida. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) que contiene y recibe información sobre el código de notificación. El miembro **dwFlag** de esta estructura indica qué dimensión se está calculando. Dependiendo del valor de **dwFlag**, debe colocar la dimensión deseada en el miembro **iWidth** o **iHeight** de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





