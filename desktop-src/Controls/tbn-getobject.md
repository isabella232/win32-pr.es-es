---
title: Código de notificación de TBN_GETOBJECT (commctrl. h)
description: Se envía mediante un control de barra de herramientas que usa el \_ estilo TBSTYLE REGISTERDROP para solicitar un objeto de destino de colocación cuando el puntero pasa sobre uno de sus botones. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- TBN_GETOBJECT controles de código de notificación de Windows
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
ms.openlocfilehash: 1ed144245e351ca4e872128e68fe658bde7c0066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149883"
---
# <a name="tbn_getobject-notification-code"></a>TBN \_ código de notificación GETOBJECT

Se envía mediante un control de barra de herramientas que usa el estilo [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) para solicitar un objeto de destino de colocación cuando el puntero pasa sobre uno de sus botones. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contiene información sobre el botón que el puntero pasó y recibe los datos que proporciona la aplicación en respuesta a este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El procesamiento de la aplicación en este código de notificación debe devolver cero.

## <a name="remarks"></a>Observaciones

Para proporcionar un objeto, una aplicación debe establecer valores en algunos miembros de la estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) en *lParam*. El miembro **pObject** debe establecerse en un puntero de objeto válido y el miembro **hResult** debe establecerse en una marca Success. Para cumplir los estándares del modelo de objetos componentes (COM), aumente siempre el recuento de referencias del objeto al proporcionar un puntero de objeto.

Si una aplicación no proporciona un objeto, debe establecer **pObject** en **null** y **hResult** en una marca de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





