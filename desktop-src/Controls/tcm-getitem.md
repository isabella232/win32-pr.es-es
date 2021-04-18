---
title: Mensaje de TCM_GETITEM (commctrl. h)
description: Recupera información sobre una pestaña de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetItem.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- TCM_GETITEM controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658355"
---
# <a name="tcm_getitem-message"></a>\_Mensaje GETITEM de TCM

Recupera información sobre una pestaña de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la pestaña.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que especifica la información que se va a recuperar y recibe información sobre la ficha. Cuando se envía el mensaje, el miembro de la **máscara** especifica los atributos que se van a devolver. Si el miembro **Mask** especifica el \_ valor de texto TCIF, el miembro **miembros pszText** debe contener la dirección del búfer que recibe el texto del elemento y el miembro **cchTextMax** debe especificar el tamaño del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Si la \_ marca de texto TCIF se establece en el miembro **Mask** de la estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , el control puede cambiar el miembro **miembros pszText** de la estructura para que apunte al nuevo texto en lugar de llenar el búfer con el texto solicitado. El control puede establecer el miembro **miembros pszText** en **null** para indicar que no hay texto asociado al elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TCM \_ GETITEMW** (Unicode) y **TCM \_ GETITEMA** (ANSI)<br/>                   |



 

 





