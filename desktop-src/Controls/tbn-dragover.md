---
title: Código de notificación de TBN_DRAGOVER (commctrl. h)
description: Determina si \_ se debe enviar un mensaje TB MARKBUTTON para un botón que se está arrastrando. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489796"
---
# <a name="tbn_dragover-notification-code"></a>\_Código de notificación TBN DRAGOVER

Determina si se debe enviar un mensaje [**TB \_ MARKBUTTON**](tb-markbutton.md) para un botón que se está arrastrando. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) que especifica el elemento sobre el que se está arrastrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**False** si la barra de herramientas debe enviar un \_ mensaje TB MARKBUTTON; de lo contrario, **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





