---
title: TCM_SETMINTABWIDTH mensaje (Commctrl.h)
description: Establece el ancho mínimo de los elementos de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetMinTabWidth.
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- TCM_SETMINTABWIDTH controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1136afa6952c30c51b619636e938b7887cd9dcf55da8d3f2d9c585ba9e1d82c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104705"
---
# <a name="tcm_setmintabwidth-message"></a>Mensaje \_ SETMINTABWIDTH de TCM

Establece el ancho mínimo de los elementos de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetMinTabWidth.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Ancho mínimo que se va a establecer para un elemento de control de pestaña. Si este parámetro se establece en -1, el control usará el ancho de tabulación predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que representa el ancho de tabulación mínimo anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





