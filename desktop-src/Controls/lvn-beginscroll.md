---
title: LVN_BEGINSCROLL de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista cuando se inicia una operación de desplazamiento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 67123db1-118c-43d7-8511-12a3c4413958
keywords:
- LVN_BEGINSCROLL código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_BEGINSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae09a05525ac6e9f08d8cc7a0b7de6ef51329baa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362614"
---
# <a name="lvn_beginscroll-notification-code"></a>Código de notificación \_ DE LVN BEGINSCROLL

Notifica a la ventana primaria de un control de vista de lista cuando se inicia una operación de desplazamiento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_BEGINSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) que contiene la posición horizontal o vertical de donde se inicia la operación de desplazamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor devuelto no utilizado.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





