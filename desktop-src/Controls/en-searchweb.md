---
title: EN_SEARCHWEB de notificación (CommCtrl.h)
description: Se envía cuando un control de edición pierde el foco del teclado. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje WM \_ NOTIFY.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062021"
---
# <a name="en_searchweb-notification-code"></a>Código de notificación EN \_ SEARCHWEB

Se envía después de que un control de edición realizara una búsqueda web cuando la característica "Buscar en la web" [está habilitada, vea EM_ENABLESEARCHWEB](em-enablesearchweb.md). La ventana primaria del control de edición recibe este código de notificación a través de un [**mensaje WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del control de edición.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMSEARCHWEB.**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ ENABLESEARCHWEB**](em-enablesearchweb.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





