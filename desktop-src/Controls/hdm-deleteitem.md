---
title: HDM_DELETEITEM mensaje (Commctrl.h)
description: Elimina un elemento de un control de encabezado. Puede enviar este mensaje explícitamente o usar la \_ macro DeleteItem de encabezado.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- HDM_DELETEITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a3ec4b48c3dcc77579f70d26cd55b7127f5a6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061998"
---
# <a name="hdm_deleteitem-message"></a>Mensaje \_ DELETEITEM de HDM

Elimina un elemento de un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro [**\_ DeleteItem de**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) encabezado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento que se eliminará.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





