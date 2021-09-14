---
title: HDN_BEGINDRAG de notificación (Commctrl.h)
description: Enviado por un control de encabezado cuando se ha iniciado una operación de arrastre en uno de sus elementos. Este código de notificación solo se envía mediante controles de encabezado que están establecidos en el estilo \_ DRAGDROP de HDS. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- HDN_BEGINDRAG código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6b4af8e662a8a9891e9a81535de987337567f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061960"
---
# <a name="hdn_begindrag-notification-code"></a>Código de notificación \_ BEGINDRAG de HDN

Enviado por un control de encabezado cuando se ha iniciado una operación de arrastre en uno de sus elementos. Este código de notificación solo se envía mediante controles de encabezado que están establecidos en el [**estilo \_ DRAGDROP de HDS.**](header-control-styles.md) Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el elemento de encabezado que se está arrastrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para permitir que el control de encabezado administre automáticamente las operaciones de arrastrar y colocar, devuelva **FALSE.** Si el propietario del control realiza manualmente la reordenación de arrastrar y colocar, devuelva **TRUE.**

## <a name="remarks"></a>Observaciones

De forma predeterminada, un control de encabezado administra automáticamente la reordenación de arrastrar y colocar. Devolver **TRUE** para indicar la administración externa (manual) de arrastrar y colocar permite al propietario del control proporcionar servicios personalizados como parte del proceso de arrastrar y colocar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





