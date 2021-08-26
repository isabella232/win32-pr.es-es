---
title: TBN_WRAPACCELERATOR de notificación (Commctrl.h)
description: Solicita el índice del botón en una o varias barras de herramientas correspondientes al carácter de acelerador especificado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c5ec222f387108e2cb4d240e6dddf0fcb904d814097a96624a177425eb805ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105035"
---
# <a name="tbn_wrapaccelerator-notification-code"></a>Código de notificación \_ WRAPACCELERATOR de TBN

Solicita el índice del botón en una o varias barras de herramientas correspondientes al carácter de acelerador especificado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que contiene el carácter de tecla de aceleración y que recibe el índice del botón correspondiente. El índice es -1 si el acelerador no se corresponde con un comando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TRUE** si se devuelve un índice; de lo **contrario, FALSE.**

## <a name="remarks"></a>Comentarios

Las aplicaciones con una o varias barras de herramientas pueden recibir este código de notificación.

La aplicación debe definir la estructura **NMTBWRAPACCELERATOR** de la siguiente manera:

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





