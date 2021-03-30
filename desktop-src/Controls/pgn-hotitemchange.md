---
title: Mensaje de PGN_HOTITEMCHANGE (commctrl. h)
description: Notifica a la ventana primaria de un control de paginación que el elemento activo (resaltado) ha cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- PGN_HOTITEMCHANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 573f3dd93a6e4b0b3db6682d36804416d6f6f1e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079265"
---
# <a name="pgn_hotitemchange-message"></a>PGN \_ HOTITEMCHANGE

Notifica a la ventana primaria de un control de paginación que el elemento activo (resaltado) ha cambiado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) que contiene información sobre este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para resaltar el elemento o un valor distinto de cero para evitar el resaltado.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





