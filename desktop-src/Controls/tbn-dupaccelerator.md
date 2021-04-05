---
title: Código de notificación de TBN_DUPACCELERATOR (commctrl. h)
description: Determina si se puede usar una tecla de aceleración en dos o más barras de herramientas activas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- TBN_DUPACCELERATOR controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079601"
---
# <a name="tbn_dupaccelerator-notification-code"></a>Código de notificación de DUPACCELERATOR de TBN \_

Determina si se puede usar una tecla de aceleración en dos o más barras de herramientas activas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


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

Devuelve **true** si es correcto; de lo contrario, **es false**.

## <a name="remarks"></a>Observaciones

La aplicación debe declarar la estructura **NMTBDUPACCELERATOR** como se indica a continuación:

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





