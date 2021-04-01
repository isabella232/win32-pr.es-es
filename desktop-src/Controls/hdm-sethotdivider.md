---
title: Mensaje de HDM_SETHOTDIVIDER (commctrl. h)
description: Cambia el color de un divisor entre los elementos de encabezado para indicar el destino de una operación externa de arrastrar y colocar. Puede enviar este mensaje explícitamente o utilizar la \_ macro header SetHotDivider.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- HDM_SETHOTDIVIDER controles de mensajes de Windows
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
ms.openlocfilehash: feb894100878e9b3ee85e8e8367a4b81a022a0a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150229"
---
# <a name="hdm_sethotdivider-message"></a>HDM \_ SETHOTDIVIDER

Cambia el color de un divisor entre los elementos de encabezado para indicar el destino de una operación externa de arrastrar y colocar. Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de valor representado por *lParam*. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                    | Significado                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Indica que *lParam* contiene las coordenadas de cliente del puntero.<br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Indica que *lParam* contiene un valor de índice de división.<br/>                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Un valor contenido en *lParam* se interpreta en función del valor de *wParam*.

Si *wParam* es **true**, *lParam* representa las coordenadas x e y del puntero. La coordenada x está en la palabra baja y la coordenada y está en la palabra alta. Cuando el control de encabezado recibe el mensaje, resalta el divisor adecuado en función de las coordenadas *lParam* .

Si *wParam* es **false**, *lParam* representa el índice entero del divisor que se va a resaltar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor igual al índice del divisor que resaltó el control.

## <a name="remarks"></a>Observaciones

Este mensaje crea un efecto de que un control de encabezado produce automáticamente cuando tiene el estilo de controlador de [**HDS \_**](header-control-styles.md) . El **mensaje \_ SETHOTDIVIDER de HDM** está diseñado para usarse cuando el propietario del control administra las operaciones de arrastrar y colocar manualmente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





