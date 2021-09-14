---
title: TDM_SET_PROGRESS_BAR_STATE mensaje (Commctrl.h)
description: Establece el estado de la barra de progreso en un cuadro de diálogo de tarea.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- TDM_SET_PROGRESS_BAR_STATE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166110"
---
# <a name="tdm_set_progress_bar_state-message"></a>Mensaje TDM \_ SET \_ PROGRESS BAR \_ \_ STATE

Establece el estado de la barra de progreso en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Un **valor int** que especifica el estado de la barra de progreso. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                   | Significado                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ NORMAL**</dt> </dl> | Establece la barra de progreso en el estado normal.<br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST \_ EN PAUSA**</dt> </dl>    | Establece la barra de progreso en el estado en pausa.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**PBST \_ ERROR**</dt> </dl>    | Establezca la barra de progreso en el estado de error.<br/>   |



 

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a GetLastError.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





