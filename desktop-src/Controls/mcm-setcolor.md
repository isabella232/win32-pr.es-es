---
title: Mensaje de MCM_SETCOLOR (commctrl. h)
description: Establece el color para una parte determinada de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetColor.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- MCM_SETCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476aafd8356359cf6b4313f4b945253af6b493c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151055"
---
# <a name="mcm_setcolor-message"></a>Mensaje de MCM \_ SETCOLOR

Establece el color para una parte determinada de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de tipo **int** que especifica el color de calendario mensual que se va a establecer. Este valor puede ser uno de los siguientes:



| Value                                                                                                                                                                     | Significado                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**Fondo de MCSC \_**</dt> </dl>       | Establecer el color de fondo que se muestra entre meses.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Establece el color de fondo que se muestra en el mes.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**\_texto MCSC**</dt> </dl>                         | Establece el color usado para mostrar el texto dentro de un mes.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Establezca el color de fondo que se muestra en el título del calendario.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | Establece el color utilizado para mostrar texto en el título del calendario.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Establezca el color usado para mostrar el texto del día del encabezado y el de los días finales. Los días de encabezado y final son los días desde los meses anterior y siguiente que aparecen en el calendario mensual actual.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el color que se establecerá para el área especificada del calendario mensual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa la configuración de color anterior para la parte especificada del control de calendario mensual si se realiza correctamente. De lo contrario, el valor devuelto es-1.

## <a name="remarks"></a>Observaciones

Si los estilos visuales están activos, este mensaje no tiene ningún efecto excepto cuando *wParam* es MCSC \_ background.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

