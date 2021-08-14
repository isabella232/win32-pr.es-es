---
title: HDM_SETITEM mensaje (Commctrl.h)
description: Establece los atributos del elemento especificado en un control de encabezado. Puede enviar este mensaje explícitamente o usar la \_ macro SetItem de encabezado.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- HDM_SETITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd0e2709a1b40bd4a564498cd0ae0b5d4e11861066aa9b0951815f92ee1c295f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171070"
---
# <a name="hdm_setitem-message"></a>Mensaje \_ SETITEM de HDM

Establece los atributos del elemento especificado en un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro [**\_ SetItem de**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) encabezado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice actual del elemento cuyos atributos se van a cambiar.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que contiene información de elementos. Cuando se envía este mensaje, se debe establecer el miembro **mask** de la estructura para indicar qué atributos se establecen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se ha hecho correctamente o cero en caso contrario.

## <a name="remarks"></a>Comentarios

La [**estructura HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que admite este mensaje admite información sobre el orden de los elementos y la lista de imágenes. Mediante el uso de estos miembros, puede controlar el orden en el que se muestran los elementos y especificar imágenes para que aparezcan con los elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDM \_ SETITEMW** (Unicode) y **HDM \_ SETITEMA** (ANSI)<br/>                   |



 

 





