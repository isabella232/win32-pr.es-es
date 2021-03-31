---
title: Mensaje de HDM_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtiene el rectángulo delimitador del botón de expansión de un elemento de encabezado con el estilo HDF \_ SPLITBUTTON. Envíe este mensaje explícitamente o mediante la \_ macro header GetItemDropDownRect.
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- HDM_GETITEMDROPDOWNRECT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079404"
---
# <a name="hdm_getitemdropdownrect-message"></a>HDM \_ GETITEMDROPDOWNRECT

Obtiene el rectángulo delimitador del botón de expansión de un elemento de encabezado con el estilo **HDF \_ SPLITBUTTON**. Envíe este mensaje explícitamente o mediante la macro [**Header \_ GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Índice de base cero del elemento de control de encabezado para el que se va a recuperar el rectángulo delimitador.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**Rect**](/windows/win32/api/windef/ns-windef-rect) que recibe la información del rectángulo delimitador. El remitente del mensaje es responsable de la asignación de esta estructura. Las coordenadas devueltas en la estructura RECT se expresan en relación con el elemento primario del control de encabezado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

El elemento de encabezado debe tener el estilo **HDF \_ SPLITBUTTON**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Acerca de los controles de encabezado](header-controls.md)
</dt> </dl>

 

 





