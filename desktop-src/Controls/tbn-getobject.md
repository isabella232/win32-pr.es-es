---
title: TBN_GETOBJECT de notificación (Commctrl.h)
description: Enviado por un control de barra de herramientas que usa el estilo TBSTYLE REGISTERDROP para solicitar un objeto de destino de colocación cuando el puntero \_ pasa sobre uno de sus botones. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- TBN_GETOBJECT código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c50f3d403089ca7db42ab89232e57d68121424c066914c534ba13a826adb8ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876735"
---
# <a name="tbn_getobject-notification-code"></a>Código de notificación GETOBJECT de TBN \_

Enviado por un control de barra de herramientas que usa el estilo [**\_ TBSTYLE REGISTERDROP**](toolbar-control-and-button-styles.md) para solicitar un objeto de destino de colocación cuando el puntero pasa sobre uno de sus botones. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contiene información sobre el botón que el puntero pasó y recibe los datos que la aplicación proporciona en respuesta a este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación que procesa este código de notificación debe devolver cero.

## <a name="remarks"></a>Comentarios

Para proporcionar un objeto , una aplicación debe establecer valores en algunos miembros de la estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) en *lParam*. El **miembro pObject** debe establecerse en un puntero de objeto válido y el **miembro hResult** debe establecerse en una marca de éxito. Para cumplir con los estándares del Modelo de objetos componentes (COM), incremente siempre el recuento de referencias del objeto al proporcionar un puntero de objeto.

Si una aplicación no proporciona un objeto , debe establecer **pObject** en **NULL** y **hResult** en una marca de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





