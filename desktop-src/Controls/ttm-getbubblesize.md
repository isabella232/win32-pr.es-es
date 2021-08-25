---
title: TTM_GETBUBBLESIZE mensaje (Commctrl.h)
description: Devuelve el ancho y alto de un control de información sobre herramientas.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- TTM_GETBUBBLESIZE controles de Windows mensaje
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
ms.openlocfilehash: 8354a93521b6adac9306374f5bfbc99e84738ac87f0471a22f199b7b611f100b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769385"
---
# <a name="ttm_getbubblesize-message"></a>Mensaje \_ GETBUBBLESIZE de TTM

Devuelve el ancho y alto de un control de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la estructura [**TOOLINFO de**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) información sobre herramientas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho de la información sobre herramientas en la palabra baja y el alto de la palabra alta si se realiza correctamente. De lo contrario, devuelve **FALSE.**

## <a name="remarks"></a>Comentarios

Si las marcas TTF TRACK y TTF ABSOLUTE se establecen en el miembro \_ \_ **uFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de información sobre herramientas, este mensaje se puede usar para ayudar a colocar la información sobre herramientas con precisión.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





