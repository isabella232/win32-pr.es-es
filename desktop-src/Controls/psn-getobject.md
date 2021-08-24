---
title: PSN_GETOBJECT de notificación (Prsht.h)
description: Enviado por una hoja de propiedades para solicitar un objeto de destino de colocación cuando el cursor pasa sobre uno de los botones del control de ficha. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- PSN_GETOBJECT código de notificación Windows controles
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81803a950c7b8eb9a41d31178c8f57d7e4199f802538616d4ced20c5a5cb4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798635"
---
# <a name="psn_getobject-notification-code"></a>Código de notificación GETOBJECT de PSN \_

Enviado por una hoja de propiedades para solicitar un objeto de destino de colocación cuando el cursor pasa sobre uno de los botones del control de ficha. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que, en la entrada, contiene información sobre el código de notificación. Si se procesa este código de notificación, debe insertar información de objeto en esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación que procesa este código de notificación debe devolver cero.

## <a name="remarks"></a>Comentarios

Para proporcionar un objeto , una aplicación debe establecer valores en algunos miembros de la estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) en *lParam*. El **miembro pObject** debe establecerse en un puntero de objeto válido y el **miembro hResult** debe establecerse en una marca de éxito. Para cumplir con los estándares del Modelo de objetos componentes (COM), incremente siempre el recuento de referencias del objeto al proporcionar un puntero de objeto.

Si una aplicación no proporciona un objeto , debe establecer **pObject** en **NULL** y **hResult** en una marca de error.

> [!Note]  
> Este código de notificación no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





