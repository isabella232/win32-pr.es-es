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
ms.openlocfilehash: b6f94f26a0893416847df052ff47731391a86f5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166262"
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

Puntero a una [**estructura TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que especifica la información que se va a recuperar y recibe información sobre la pestaña. Cuando se envía el mensaje, el **miembro mask** especifica qué atributos se devuelven. Si el miembro **mask** especifica el valor TCIF TEXT, el miembro pszText debe contener la dirección del búfer que recibe el texto del elemento y el miembro \_  **cchTextMax** debe especificar el tamaño del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Observaciones

Si la marca TCIF TEXT se establece en el miembro mask de la estructura TCITEM, el control puede cambiar el miembro \_ **pszText**  de la estructura para que apunte al nuevo texto en lugar de rellenar el búfer con el texto solicitado. [](/windows/win32/api/commctrl/ns-commctrl-tcitema) El control puede establecer el **miembro pszText** en **NULL** para indicar que no hay ningún texto asociado al elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TCM \_ GETITEMW** (Unicode) y **TCM \_ GETITEMA** (ANSI)<br/>                   |



 

 





