---
title: Código de notificación de EN_SEARCHWEB (CommCtrl. h)
description: Se envía cuando un control de edición pierde el foco del teclado. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de notificación de WM \_ .
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489280"
---
# <a name="en_searchweb-notification-code"></a>\_Código de notificación en SEARCHWEB

Enviado después de que un control de edición realice una búsqueda web cuando la característica "Buscar en la web" esté habilitada, vea [EM_ENABLESEARCHWEB](em-enablesearchweb.md). La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de notificación de [**WM \_**](wm-notify.md) .


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

Puntero a una estructura [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2019 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_ENABLESEARCHWEB em**](em-enablesearchweb.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**\_notificaciones de WM**](wm-notify.md)
</dt> </dl>

 

 





