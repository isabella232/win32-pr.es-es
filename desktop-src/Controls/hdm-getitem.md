---
title: HDM_GETITEM mensaje (Commctrl.h)
description: Obtiene información sobre un elemento de un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro Header \_ GetItem.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- HDM_GETITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 566f8b8e3bdf4e92abfb1fdd5874b8514814792e1d7aae169cc2aca4b2e8d101
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436195"
---
# <a name="hdm_getitem-message"></a>Mensaje \_ GETITEM de HDM

Obtiene información sobre un elemento de un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro [**Header \_ GetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento para el que se va a recuperar la información.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura HDITEM.**](/windows/win32/api/commctrl/ns-commctrl-hditema) Cuando se envía el mensaje, el **miembro mask** indica el tipo de información que se solicita. Cuando se devuelve el mensaje, los demás miembros reciben la información solicitada. Si el **miembro mask** especifica cero, el mensaje devuelve **TRUE** pero no copia ninguna información en la estructura .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

Si la marca HDI TEXT se establece en el miembro mask de la estructura HDITEM, el control puede cambiar el miembro \_ **pszText**  de la estructura para que apunte al nuevo texto en lugar de rellenar el búfer con el texto solicitado. [](/windows/win32/api/commctrl/ns-commctrl-hditema) Las aplicaciones no deben suponer que el texto siempre se colocará en el búfer solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDM \_ GETITEMW** (Unicode) y **HDM \_ GETITEMA** (ANSI)<br/>                   |



 

 





