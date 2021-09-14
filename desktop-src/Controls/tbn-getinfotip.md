---
title: TBN_GETINFOTIP de notificación (Commctrl.h)
description: Recupera información sobre información sobre un elemento de la barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166345"
---
# <a name="tbn_getinfotip-notification-code"></a>Código de notificación \_ DE TBN GETINFOTIP

Recupera información sobre información sobre un elemento de la barra de herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) que contiene información de elementos y recibe información sobre información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto.

## <a name="remarks"></a>Observaciones

La compatibilidad con la información sobre la información en la barra de herramientas permite que la barra de herramientas muestre información sobre herramientas para elementos tan grandes como los caracteres INFOTIPSIZE. Si no se procesa este código de notificación, la barra de herramientas usará el texto del elemento para la información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TBN \_ GETINFOTIPW** (Unicode) y **TBN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





