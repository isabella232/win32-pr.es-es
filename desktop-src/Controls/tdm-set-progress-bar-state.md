---
title: Mensaje de TDM_SET_PROGRESS_BAR_STATE (commctrl. h)
description: Establece el estado de la barra de progreso en un cuadro de diálogo de tarea.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- TDM_SET_PROGRESS_BAR_STATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f0ae4ec104c8472d3640aa804650640d77cc63
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2021
ms.locfileid: "104362006"
---
# <a name="tdm_set_progress_bar_state-message"></a>Mensaje de estado de la barra de progreso del conjunto de TDM \_ \_ \_ \_

Establece el estado de la barra de progreso en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Un valor **int** que especifica el estado de la barra de progreso. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                   | Significado                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ normal**</dt> </dl> | Establece la barra de progreso en el estado normal.<br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST en \_ pausa**</dt> </dl>    | Establece la barra de progreso en el estado de pausa.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**\_error PBST**</dt> </dl>    | Establezca la barra de progreso en el estado de error.<br/>   |



 

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a GetLastError.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





