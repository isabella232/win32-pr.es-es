---
title: Mensaje de TTM_GETBUBBLESIZE (commctrl. h)
description: Devuelve el ancho y el alto de un control ToolTip.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- TTM_GETBUBBLESIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150309"
---
# <a name="ttm_getbubblesize-message"></a>TTM \_ GETBUBBLESIZE

Devuelve el ancho y el alto de un control ToolTip.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de la información sobre herramientas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho de la información sobre herramientas en la palabra baja y la altura de la palabra alta si se realiza correctamente. De lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Si las \_ marcas de seguimiento y ttf de ttf \_ se establecen en el miembro **uFlags** de la estructura ToolTip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , este mensaje se puede usar para ayudar a colocar la información sobre herramientas con precisión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





