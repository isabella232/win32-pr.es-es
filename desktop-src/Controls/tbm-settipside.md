---
title: TBM_SETTIPSIDE mensaje (Commctrl.h)
description: Coloca un control de información sobre herramientas utilizado por un control trackbar. Los controles de barra de seguimiento que usan el estilo TBS \_ TOOLTIPS muestran información sobre herramientas.
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- TBM_SETTIPSIDE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166409"
---
# <a name="tbm_settipside-message"></a>Mensaje \_ SETTIPSIDE de TBM

Coloca un control de información sobre herramientas utilizado por un control trackbar. Los controles de barra de seguimiento que usan el estilo [**TBS \_ TOOLTIPS**](trackbar-control-styles.md) muestran información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que representa la ubicación en la que se va a mostrar el control de información sobre herramientas. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                                   | Significado                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <dt>**TBTS \_ TOP**</dt> </dl>          | El control de información sobre herramientas se colocará encima de la barra de seguimiento. Esta marca se usa con barras de seguimiento horizontales.<br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <dt>**TBTS \_ LEFT**</dt> </dl>       | El control de información sobre herramientas se colocará a la izquierda de la barra de seguimiento. Esta marca se usa con barras de seguimiento verticales.<br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <dt>**TBTS \_ BOTTOM**</dt> </dl> | El control de información sobre herramientas se colocará debajo de la barra de seguimiento. Esta marca se usa con barras de seguimiento horizontales.<br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <dt>**DERECHO DE \_ TBTS**</dt> </dl>    | El control de información sobre herramientas se colocará a la derecha de la barra de seguimiento. Esta marca se usa con barras de seguimiento verticales.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor que representa la ubicación anterior del control de información sobre herramientas. El valor devuelto es igual a uno de los valores posibles para *wParam.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





