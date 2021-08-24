---
title: HDM_SETHOTDIVIDER mensaje (Commctrl.h)
description: Cambia el color de un divisor entre los elementos de encabezado para indicar el destino de una operación externa de arrastrar y colocar. Puede enviar este mensaje explícitamente o usar la \_ macro SetHotDivider de encabezado.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- HDM_SETHOTDIVIDER controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedfca7a6f0d10651984efb63c4db63116c4a53d2b9f9b85905c93fc12e6ca16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544755"
---
# <a name="hdm_sethotdivider-message"></a>Mensaje \_ SETHOTDIVIDER de HDM

Cambia el color de un divisor entre los elementos de encabezado para indicar el destino de una operación externa de arrastrar y colocar. Puede enviar este mensaje explícitamente o usar la macro [**\_ SetHotDivider de encabezado.**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de valor representado por *lParam*. Este valor puede ser uno de los siguientes:



| Valor                                                                                                                                    | Significado                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE**</dt> </dl>    | Indica que *lParam contiene* las coordenadas de cliente del puntero.<br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE**</dt> </dl> | Indica que *lParam* contiene un valor de índice de divisor.<br/>                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Un valor mantenido en *lParam* se interpreta según el valor de *wParam*.

Si *wParam es* **TRUE,** *lParam* representa las coordenadas x e y del puntero. La coordenada x está en la palabra baja y la coordenada Y está en la palabra alta. Cuando el control de encabezado recibe el mensaje, resalta el divisor adecuado en función de las coordenadas *lParam.*

Si *wParam* es **FALSE,** *lParam* representa el índice entero del divisor que se va a resaltar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor igual al índice del divisor resaltado por el control.

## <a name="remarks"></a>Comentarios

Este mensaje crea un efecto que un control de encabezado genera automáticamente cuando tiene el estilo [**\_ DRAGDROP de HDS.**](header-control-styles.md) El **mensaje \_ SETHOTDIVIDER** de HDM está pensado para usarse cuando el propietario del control controla manualmente las operaciones de arrastrar y colocar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





