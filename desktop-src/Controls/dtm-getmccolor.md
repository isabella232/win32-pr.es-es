---
title: DTM_GETMCCOLOR mensaje (Commctrl.h)
description: Obtiene el color de una parte determinada del calendario mensual dentro de un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la \_ macro DateTime GetMonthCalColor.
ms.assetid: 892e8c23-f0d0-4fd6-98ed-39592c4d316f
keywords:
- DTM_GETMCCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- DTM_GETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99a67f6ca7056f0157d131d185cb5cb68a85e06b8cbb124a16b3c2129c21963
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878155"
---
# <a name="dtm_getmccolor-message"></a>Mensaje \_ GETMCCOLOR de DTM

Obtiene el color de una parte determinada del calendario mensual dentro de un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**\_ DateTime GetMonthCalColor.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de tipo **int** que especifica el color del calendario mensual que se va a recuperar. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                                                     | Significado                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**MCSC \_ BACKGROUND**</dt> </dl>       | Recupere el color de fondo mostrado entre meses.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Recupere el color de fondo que se muestra en el mes.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**TEXTO DE \_ MCSC**</dt> </dl>                         | Recupere el color utilizado para mostrar texto en un mes.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Recupere el color de fondo que se muestra en el título del calendario.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**TITLETEXT de MCSC \_**</dt> </dl>          | Recupere el color utilizado para mostrar texto dentro del título del calendario.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Recupere el color utilizado para mostrar el día del encabezado y el texto del día final. Los días de encabezado y final son los días de los meses anteriores y siguientes que aparecen en el calendario del mes actual.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor COLORREF que** representa la configuración de color para la parte especificada del control de calendario mensual si se realiza correctamente. El mensaje devuelve -1 si no se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





