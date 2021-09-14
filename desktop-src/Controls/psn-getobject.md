---
title: PSN_GETOBJECT de notificación (Prsht.h)
description: Enviado por una hoja de propiedades para solicitar un objeto de destino de colocación cuando el cursor pasa sobre uno de los botones del control de pestaña. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- PSN_GETOBJECT de notificación Windows controles
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
ms.openlocfilehash: d0a039cf97dee1d1f1168894bb167c06de10d38d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167454"
---
# <a name="psn_getobject-notification-code"></a>Código de notificación GETOBJECT de PSN \_

Enviado por una hoja de propiedades para solicitar un objeto de destino de colocación cuando el cursor pasa sobre uno de los botones del control de pestaña. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


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

## <a name="remarks"></a>Observaciones

Para proporcionar un objeto , una aplicación debe establecer valores en algunos miembros de la estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) en *lParam*. El **miembro pObject** debe establecerse en un puntero de objeto válido y el **miembro hResult** debe establecerse en una marca de éxito. Para cumplir con los estándares del Modelo de objetos componentes (COM), incremente siempre el recuento de referencias del objeto al proporcionar un puntero de objeto.

Si una aplicación no proporciona un objeto , debe establecer **pObject** en **NULL** y **hResult** en una marca de error.

> [!Note]  
> Este código de notificación no se admite cuando se usa el estilo del asistente de Aero [**(PSH \_ AEROWIZARD).**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





