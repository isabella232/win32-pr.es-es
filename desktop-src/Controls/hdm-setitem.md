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
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061972"
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

## <a name="remarks"></a>Observaciones

La [**estructura HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que admite este mensaje admite información sobre el orden de los elementos y la lista de imágenes. Mediante el uso de estos miembros, puede controlar el orden en el que se muestran los elementos y especificar imágenes para que aparezcan con los elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDM \_ SETITEMW** (Unicode) y **HDM \_ SETITEMA** (ANSI)<br/>                   |



 

 





