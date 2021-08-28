---
title: MCM_SETCOLOR mensaje (Commctrl.h)
description: Establece el color de una parte determinada de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetColor.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- MCM_SETCOLOR controles de Windows mensaje
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
ms.openlocfilehash: 0915f78ad2dc666d6476cebb51be4f8b8c6102cb1433da59af7b9a1342deedc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697155"
---
# <a name="mcm_setcolor-message"></a>Mensaje \_ SETCOLOR de MCM

Establece el color de una parte determinada de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetColor.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de tipo **int** que especifica el color del calendario mensual que se va a establecer. Este valor puede ser uno de los siguientes:



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                            |
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

[**Valor COLORREF**](/windows/desktop/gdi/colorref) que representa el color que se establecerá para el área especificada del calendario mensual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un [**valor COLORREF que**](/windows/desktop/gdi/colorref) representa la configuración de color anterior para la parte especificada del control de calendario mensual si se realiza correctamente. De lo contrario, la devolución es -1.

## <a name="remarks"></a>Comentarios

Si los estilos visuales están activos, este mensaje no tiene ningún efecto excepto cuando *wParam* es MCSC \_ BACKGROUND.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

