---
title: DTM_SETMCCOLOR mensaje (Commctrl.h)
description: Establece el color de una parte determinada del calendario mensual dentro de un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro DateTime \_ SetMonthCalColor.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- DTM_SETMCCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- DTM_SETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e496abb4dd28b040dd4a8035073ffa32a3f3847
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172021"
---
# <a name="dtm_setmccolor-message"></a>Mensaje \_ SETMCCOLOR de DTM

Establece el color de una parte determinada del calendario mensual dentro de un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ SetMonthCalColor.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de tipo **int** que especifica el color del calendario mensual que se va a establecer. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                                                     | Significado                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**FONDO DE \_ MCSC**</dt> </dl>       | Establezca el color de fondo que se muestra entre meses.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Establezca el color de fondo que se muestra en el mes.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**MCSC \_ TEXT**</dt> </dl>                         | Establezca el color utilizado para mostrar texto en un mes.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Establezca el color de fondo que se muestra en el título del calendario.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**TITLETEXT de MCSC \_**</dt> </dl>          | Establezca el color utilizado para mostrar texto dentro del título del calendario.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Establezca el color utilizado para mostrar el día del encabezado y el texto del día final. Los días de encabezado y final son los días de los meses anteriores y siguientes que aparecen en el calendario del mes actual.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **COLORREF que** representa el color que se establecerá para el área especificada del calendario mensual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor COLORREF que** representa la configuración de color anterior para la parte especificada del control de calendario mensual si se realiza correctamente. De lo contrario, el mensaje devuelve -1.

## <a name="remarks"></a>Observaciones

Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto excepto cuando *wParam* es MCSC \_ BACKGROUND.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





