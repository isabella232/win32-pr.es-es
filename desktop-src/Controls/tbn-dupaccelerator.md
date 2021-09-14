---
title: TBN_DUPACCELERATOR de notificación (Commctrl.h)
description: Determina si se puede usar una tecla de aceleración en dos o más barras de herramientas activas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- TBN_DUPACCELERATOR código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e530fa2101f8145148b7ede7d74f53a1828fa58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166369"
---
# <a name="tbn_dupaccelerator-notification-code"></a>Código de notificación \_ DE TBN DUPACCELERATOR

Determina si se puede usar una tecla de aceleración en dos o más barras de herramientas activas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que proporciona un acelerador y que recibe un valor que especifica si varias barras de herramientas responden al mismo carácter.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente; de lo **contrario, FALSE.**

## <a name="remarks"></a>Observaciones

La aplicación debe declarar la **estructura NMTBDUPACCELERATOR** como se muestra a continuación:

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





