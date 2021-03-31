---
title: Mensaje de TCM_SETCURFOCUS (commctrl. h)
description: Establece el foco en una pestaña especificada de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetCurFocus.
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- TCM_SETCURFOCUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996421"
---
# <a name="tcm_setcurfocus-message"></a>\_Mensaje SETCURFOCUS de TCM

Establece el foco en una pestaña especificada de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la pestaña que obtiene el foco.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el control de pestaña tiene el estilo de [**\_ botones de TCS**](tab-control-styles.md) (modo de botón), la pestaña con el foco puede ser diferente de la pestaña seleccionada. Por ejemplo, cuando se selecciona una pestaña, el usuario puede presionar las teclas de dirección para establecer el foco en una pestaña diferente sin cambiar la pestaña seleccionada. En el modo de botón, **TCM \_ SETCURFOCUS** establece el foco de entrada en el botón asociado a la pestaña especificada, pero no cambia la pestaña seleccionada.

Si el control de pestañas no tiene el estilo de [**\_ botones de TCS**](tab-control-styles.md) , cambiar el foco también cambia la pestaña seleccionada. En este caso, el control de pestañas envía los códigos de notificación [TCN \_ SELCHANGING](tcn-selchanging.md) y [TCN \_ SELCHANGE](tcn-selchange.md) a su ventana primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETCURFOCUS TCM**](tcm-getcurfocus.md)
</dt> </dl>

 

 





