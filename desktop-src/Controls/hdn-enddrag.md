---
title: Código de notificación de HDN_ENDDRAG (commctrl. h)
description: Lo envía un control de encabezado cuando una operación de arrastrar ha finalizado en uno de sus elementos. Este código de notificación se envía como un mensaje de notificación de WM \_ . Solo los controles de encabezado que se establecen en el \_ estilo HDS DRAGDROP envían este código de notificación.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- HDN_ENDDRAG controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493342"
---
# <a name="hdn_enddrag-notification-code"></a>Código de notificación de ENDDRAG de HDN \_

Lo envía un control de encabezado cuando una operación de arrastrar ha finalizado en uno de sus elementos. Este código de notificación se envía como un mensaje de notificación de [**WM \_**](wm-notify.md) . Solo los controles de encabezado que se establecen en el estilo [**HDS \_ DRAGDROP**](header-control-styles.md) envían este código de notificación.


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el elemento de encabezado que se estaba arrastrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para permitir que el control Coloque y reordene automáticamente el elemento, devuelva **false**. Para evitar que se coloque el elemento, devuelva **true**.

## <a name="remarks"></a>Observaciones

Si el propietario está realizando la administración externa de arrastrar y colocar (manual), debe devolver el valor **false**. Después, el propietario debe reordenar los elementos de encabezado manualmente mediante el envío de [**HDM \_ SETITEM**](hdm-setitem.md) o [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





