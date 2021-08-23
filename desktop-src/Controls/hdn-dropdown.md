---
title: HDN_DROPDOWN de notificación (Commctrl.h)
description: Enviado por un control de encabezado a su elemento primario cuando se hace clic en la flecha desplegable del control de encabezado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a5a7e423c40fa655a9eca0e5b97c20a2d61add1e6c0b7f66b65a69afdc32a55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435575"
---
# <a name="hdn_dropdown-notification-code"></a>Código de notificación \_ DE HDN DROPDOWN

Enviado por un control de encabezado a su elemento primario cuando se hace clic en la flecha desplegable del control de encabezado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

En el ejemplo de la sección Sintaxis se muestra cómo el receptor de notificaciones convierte **LPARAM** para recuperar la [**estructura NMHEADER.**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) **WPARAM** contiene el identificador del control que envía este mensaje.

Este mensaje solo se envía si el estilo HDF \_ SPLITBUTTON está establecido en el elemento de encabezado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





