---
title: TBN_WRAPHOTITEM de notificación (Commctrl.h)
description: Notifica a una aplicación con dos o más barras de herramientas que el elemento de acceso rápido está a punto de cambiar. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c6bd1f2e750a2fd71dc053d31ca452fa581891037db73d356e5405476b28de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293374"
---
# <a name="tbn_wraphotitem-notification-code"></a>Código de notificación \_ WRAPHOTITEM de TBN

Notifica a una aplicación con dos o más barras de herramientas que el elemento de acceso rápido está a punto de cambiar. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura que contiene el elemento de acceso rápido antiguo (**iStart**) y si el nuevo elemento de acceso rápido está delante de él (**iDir** = -1) o después de él (**iDir** = 1), así como un motivo por el que cambia el elemento de acceso rápido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TRUE** si la aplicación está controlando el propio cambio de elemento de acceso. en caso **contrario, FALSE**.

## <a name="remarks"></a>Comentarios

La aplicación debe definir la estructura **NMTBWRAPHOTITEM** de la siguiente manera:

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





