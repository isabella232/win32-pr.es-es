---
title: Código de notificación de HDN_BEGINDRAG (commctrl. h)
description: Lo envía un control de encabezado cuando se ha iniciado una operación de arrastre en uno de sus elementos. Este código de notificación solo lo envían los controles de encabezado que se establecen en el estilo de la de HDS \_ . Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- HDN_BEGINDRAG controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079304"
---
# <a name="hdn_begindrag-notification-code"></a>Código de notificación de BEGINDRAG de HDN \_

Lo envía un control de encabezado cuando se ha iniciado una operación de arrastre en uno de sus elementos. Este código de notificación solo lo envían los controles de encabezado que se establecen en el estilo de la de [**HDS \_**](header-control-styles.md) . Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


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

Para permitir que el control de encabezado Administre automáticamente las operaciones de arrastrar y colocar, devuelva **false**. Si el propietario del control realiza manualmente una reordenación de arrastrar y colocar, devuelve **true**.

## <a name="remarks"></a>Observaciones

Un control de encabezado tiene como valor predeterminado la administración automática de la reordenación de arrastrar y colocar. Devolver **true** para indicar que la administración de arrastrar y colocar externa (manual) permite que el propietario del control proporcione servicios personalizados como parte del proceso de arrastrar y colocar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





