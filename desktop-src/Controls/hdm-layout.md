---
title: HDM_LAYOUT mensaje (Commctrl.h)
description: Recupera la información utilizada para establecer el tamaño y la posición del control de encabezado dentro del rectángulo de destino de la ventana primaria. Puede enviar este mensaje explícitamente o usar la macro Diseño \_ de encabezado.
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- HDM_LAYOUT controles de Windows mensaje
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
ms.openlocfilehash: ff4194ad5aa1847aa977bac1269a7ab88d36a571824387e07264713726135f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435935"
---
# <a name="hdm_layout-message"></a>Mensaje DE DISEÑO DE HDM \_

Recupera la información utilizada para establecer el tamaño y la posición del control de encabezado dentro del rectángulo de destino de la ventana primaria. Puede enviar este mensaje explícitamente o usar la macro [**Diseño \_ de encabezado.**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**HDLAYOUT.**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) El **miembro prc** especifica las coordenadas de un rectángulo y el miembro **pwpos** recibe el tamaño y la posición del control de encabezado dentro del rectángulo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

El **miembro pwpos** de la estructura *lParam* recibe los valores de tamaño y posición adecuados para colocar el control en la parte superior del rectángulo especificado. El valor de alto es la suma de las alturas de los bordes horizontales del control y el alto medio de los caracteres de la fuente seleccionada actualmente en el contexto del dispositivo del control.

Para usar **HDM \_ LAYOUT para** establecer el tamaño inicial y la posición de un control de encabezado, establezca el estado de visibilidad inicial del control para que esté oculto. Después de **enviar HDM \_ LAYOUT** para recuperar los valores de tamaño y posición, use la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para establecer el nuevo tamaño, la posición y el estado de visibilidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

