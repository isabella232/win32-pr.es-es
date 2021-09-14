---
title: TCM_SETCURFOCUS mensaje (Commctrl.h)
description: Establece el foco en una pestaña especificada en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetCurFocus.
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- TCM_SETCURFOCUS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166222"
---
# <a name="tcm_setcurfocus-message"></a>Mensaje \_ SETCURFOCUS de TCM

Establece el foco en una pestaña especificada en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetCurFocus.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus)

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

Si el control de pestaña tiene el [**estilo TCS \_ BUTTONS**](tab-control-styles.md) (modo de botón), la pestaña con el foco puede ser diferente de la pestaña seleccionada. Por ejemplo, cuando se selecciona una pestaña, el usuario puede presionar las teclas de dirección para establecer el foco en otra pestaña sin cambiar la pestaña seleccionada. En el modo de botón, **TCM \_ SETCURFOCUS** establece el foco de entrada en el botón asociado a la pestaña especificada, pero no cambia la pestaña seleccionada.

Si el control de pestaña no tiene el [**estilo TCS \_ BUTTONS,**](tab-control-styles.md) cambiar el foco también cambia la pestaña seleccionada. En este caso, el control de pestaña envía los códigos de notificación [ \_ TCN SELCHANGING](tcn-selchanging.md) y [TCN \_ SELCHANGE](tcn-selchange.md) a su ventana primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TCM \_ GETCURFOCUS**](tcm-getcurfocus.md)
</dt> </dl>

 

 





