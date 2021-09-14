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
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166309"
---
# <a name="tbn_save-notification-code"></a>Código de notificación SAVE de TBN \_

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

## <a name="remarks"></a>Observaciones

La aplicación recibirá este código de notificación una vez al principio del proceso de guardado y una vez por cada botón. Este código de notificación le ofrece la oportunidad de agregar su propia información a la guardada por el Shell. Si no desea agregar información, ignore el código de notificación. Consulte [Personalización de la](toolbar-controls-overview.md) barra de herramientas para obtener una explicación más detallada de cómo controlar TBN \_ SAVE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[RESTAURACIÓN DE TBN \_](tbn-restore.md)
</dt> </dl>

 

 





