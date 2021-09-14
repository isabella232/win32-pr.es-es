---
title: HDM_GETITEMDROPDOWNRECT mensaje (Commctrl.h)
description: Obtiene el rectángulo delimitador del botón de división para un elemento de encabezado con el estilo HDF \_ SPLITBUTTON. Envíe este mensaje explícitamente o mediante la macro Header \_ GetItemDropDownRect.
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- HDM_GETITEMDROPDOWNRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061993"
---
# <a name="hdm_getitemdropdownrect-message"></a>Mensaje \_ GETITEMDROPDOWNRECT de HDM

Obtiene el rectángulo delimitador del botón de división para un elemento de encabezado con el **estilo HDF \_ SPLITBUTTON**. Envíe este mensaje explícitamente o mediante la macro [**Header \_ GetItemDropDownRect.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Índice de base cero del elemento de control de encabezado para el que se va a recuperar el rectángulo delimitador.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura RECT**](/windows/win32/api/windef/ns-windef-rect) que recibe la información del rectángulo delimitador. El remitente del mensaje es responsable de asignar esta estructura. Las coordenadas devueltas en la estructura RECT se expresan en relación con el elemento primario del control de encabezado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Observaciones

El elemento de encabezado debe tener el **estilo HDF \_ SPLITBUTTON**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Acerca de los controles de encabezado](header-controls.md)
</dt> </dl>

 

 





