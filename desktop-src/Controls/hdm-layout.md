---
title: Mensaje de HDM_LAYOUT (commctrl. h)
description: Recupera información utilizada para establecer el tamaño y la posición del control de encabezado dentro del rectángulo de destino de la ventana primaria. Puede enviar este mensaje explícitamente o utilizar la macro de diseño de encabezado \_ .
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- HDM_LAYOUT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70fc46dee52f52862136dbe583db9f6d7a0e13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079402"
---
# <a name="hdm_layout-message"></a>Mensaje de diseño de HDM \_

Recupera información utilizada para establecer el tamaño y la posición del control de encabezado dentro del rectángulo de destino de la ventana primaria. Puede enviar este mensaje explícitamente o utilizar la macro de [**\_ diseño de encabezado**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) . El miembro **PRC** especifica las coordenadas de un rectángulo y el miembro **pwpos** recibe el tamaño y la posición del control de encabezado dentro del rectángulo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

El miembro **pwpos** de la estructura *lParam* recibe los valores de tamaño y posición adecuados para colocar el control a lo largo de la parte superior del rectángulo especificado. El valor de alto es la suma de los altos de los bordes horizontales del control y el alto medio de los caracteres de la fuente actualmente seleccionada en el contexto del dispositivo del control.

Para usar **el \_ diseño de HDM** para establecer el tamaño y la posición iniciales de un control de encabezado, establezca el estado de visibilidad inicial del control para que esté oculto. Después de enviar el **\_ diseño de HDM** para recuperar los valores de tamaño y posición, utilice la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para establecer el nuevo tamaño, la posición y el estado de visibilidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

