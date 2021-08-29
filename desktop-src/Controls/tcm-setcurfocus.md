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
ms.openlocfilehash: ac3be7b9b7f62d69a1207e60f58189f152f109531d83e4f7b80b6e13ca6f6da3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876495"
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

## <a name="remarks"></a>Comentarios

Si el control de pestaña tiene el [**estilo TCS \_ BUTTONS**](tab-control-styles.md) (modo de botón), la pestaña con el foco puede ser diferente de la pestaña seleccionada. Por ejemplo, cuando se selecciona una pestaña, el usuario puede presionar las teclas de dirección para establecer el foco en otra pestaña sin cambiar la pestaña seleccionada. En el modo de botón, **TCM \_ SETCURFOCUS** establece el foco de entrada en el botón asociado a la pestaña especificada, pero no cambia la pestaña seleccionada.

Si el control de pestaña no tiene el estilo [**TCS \_ BUTTONS,**](tab-control-styles.md) cambiar el foco también cambia la pestaña seleccionada. En este caso, el control de pestaña envía los códigos de notificación [TCN \_ SELCHANGING](tcn-selchanging.md) y [TCN \_ SELCHANGE](tcn-selchange.md) a su ventana primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TCM \_ GETCURFOCUS**](tcm-getcurfocus.md)
</dt> </dl>

 

 





