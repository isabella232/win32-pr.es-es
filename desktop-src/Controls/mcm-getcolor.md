---
title: Mensaje de MCM_GETCOLOR (commctrl. h)
description: Recupera el color para una parte determinada de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetColor.
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- MCM_GETCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932b457bd1ddd870fd84facdb540e31188825504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150878"
---
# <a name="mcm_getcolor-message"></a>Mensaje de GETCOLOR de MCM \_

Recupera el color para una parte determinada de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de tipo **int** que especifica el color de calendario mensual que se va a recuperar. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                                                     | Significado                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**Fondo de MCSC \_**</dt> </dl>       | Recupera el color de fondo que se muestra entre meses.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Recupera el color de fondo que se muestra en el mes.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**\_texto MCSC**</dt> </dl>                         | Recupera el color usado para mostrar el texto dentro de un mes.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Recupera el color de fondo que se muestra en el título del calendario.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | Recupera el color usado para mostrar el texto dentro del título del calendario.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Recupera el color que se usa para mostrar el texto del día y el final del encabezado. Los días de encabezado y final son los días desde los meses anterior y siguiente que aparecen en el calendario mensual actual.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de **COLORREF** que representa la configuración de color para la parte especificada del control de calendario mensual si se realiza correctamente. De lo contrario, este mensaje devuelve-1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





