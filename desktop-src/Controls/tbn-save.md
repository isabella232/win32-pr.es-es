---
title: TBN_SAVE de notificación (Commctrl.h)
description: Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de guardarse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- TBN_SAVE código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f9d4fb40d0e5beafcd720b4de52a8cf09d17c3e4c6f7b4dcfa8da78e00e97ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876595"
---
# <a name="tbn_save-notification-code"></a>TBN \_ SAVE notification code

Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de guardarse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTBSAVE.**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La aplicación recibirá este código de notificación una vez al principio del proceso de guardado y una vez para cada botón. Este código de notificación le ofrece la oportunidad de agregar su propia información a la guardada por el shell. Si no desea agregar información, ignore el código de notificación. Consulte [Personalización de la](toolbar-controls-overview.md) barra de herramientas para obtener una explicación más detallada de cómo controlar TBN \_ SAVE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[RESTAURACIÓN DE TBN \_](tbn-restore.md)
</dt> </dl>

 

 





