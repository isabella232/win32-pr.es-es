---
title: Mensaje de TBM_SETTIPSIDE (commctrl. h)
description: Coloca un control ToolTip utilizado por un control TrackBar. Los controles de barra de control que usan el estilo información sobre herramientas de TBS \_ muestran información sobre herramientas.
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- TBM_SETTIPSIDE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422115"
---
# <a name="tbm_settipside-message"></a>TBM \_ SETTIPSIDE

Coloca un control ToolTip utilizado por un control TrackBar. Los controles de barra de control que usan el estilo [**\_ información**](trackbar-control-styles.md) sobre herramientas de TBS muestran información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que representa la ubicación en la que se va a mostrar el control ToolTip. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                                   | Significado                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <dt>**TBTS \_ superior**</dt> </dl>          | El control ToolTip se colocará sobre la barra de herramientas. Esta marca se usa con trackbars horizontal.<br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <dt>**TBTS a la \_ izquierda**</dt> </dl>       | El control ToolTip se colocará a la izquierda de la barra de herramientas. Esta marca se usa con trackbars vertical.<br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <dt>**TBTS \_ inferior**</dt> </dl> | El control ToolTip se colocará debajo de la barra de herramientas. Esta marca se usa con trackbars horizontal.<br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <dt>**TBTS \_ derecha**</dt> </dl>    | El control ToolTip se colocará a la derecha de la barra de herramientas. Esta marca se usa con trackbars vertical.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor que representa la ubicación anterior del control ToolTip. El valor devuelto es igual a uno de los valores posibles de *wParam*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





