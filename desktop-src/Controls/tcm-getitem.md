---
title: TCM_GETITEM mensaje (Commctrl.h)
description: Recupera información sobre una pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetItem.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- TCM_GETITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5403bb85e1b2747d1ab6081d33c25ec20a3b2099fc83b2b15e66b014f558584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876585"
---
# <a name="tcm_getitem-message"></a>Mensaje \_ GETITEM de TCM

Recupera información sobre una pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la pestaña.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que especifica la información que se va a recuperar y recibe información sobre la pestaña. Cuando se envía el mensaje, el **miembro mask** especifica qué atributos se devuelven. Si el miembro **mask** especifica el valor TEXT de TCIF, el miembro pszText debe contener la dirección del búfer que recibe el texto del elemento y el miembro \_  **cchTextMax** debe especificar el tamaño del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

Si la marca TEXT de TCIF se establece en el miembro mask de la estructura TCITEM, el control puede cambiar el miembro \_ **pszText**  de la estructura para que apunte al nuevo texto en lugar de rellenar el búfer con el texto solicitado. [](/windows/win32/api/commctrl/ns-commctrl-tcitema) El control puede establecer el **miembro pszText** en **NULL** para indicar que no hay ningún texto asociado al elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TCM \_ GETITEMW** (Unicode) y **TCM \_ GETITEMA** (ANSI)<br/>                   |



 

 





