---
title: Mensaje de LVM_GETITEM (commctrl. h)
description: Recupera algunos o todos los atributos de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItem de ListView.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- LVM_GETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c19632567db5e37059b1b028a8ec1fc9385268cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803397"
---
# <a name="lvm_getitem-message"></a>\_Mensaje GETITEM de LVM

Recupera algunos o todos los atributos de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que especifica la información que se va a recuperar y recibe información sobre el elemento de vista de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando se envía el mensaje **\_ GETITEM de LVM** , los miembros **iItem** y **iSubItem** identifican el elemento o subelemento del que se va a recuperar información y el miembro de **máscara** especifica los atributos que se van a recuperar. Para obtener una lista de los valores posibles, vea la descripción de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

Si la \_ marca de texto LVIF se establece en el miembro **Mask** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , el miembro **miembros pszText** debe apuntar a un búfer válido y el miembro **cchTextMax** debe establecerse en el número de caracteres de ese búfer. Las aplicaciones no deben suponer que el texto se colocará necesariamente en el búfer especificado. En su lugar, el control puede cambiar el miembro **miembros pszText** de la estructura para que apunte al nuevo texto, en lugar de colocarlo en el búfer.

Si el miembro **Mask** especifica el \_ valor de estado LVIF, el miembro **stateMask** debe especificar los bits de estado del elemento que se van a recuperar. En la salida, el miembro **State** contiene los valores de los bits de estado especificados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ GETITEMW** (Unicode) y **\_ GETITEMA de LVM** (ANSI)<br/>                   |



 

 





