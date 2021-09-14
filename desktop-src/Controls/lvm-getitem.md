---
title: LVM_GETITEM mensaje (Commctrl.h)
description: Recupera algunos o todos los atributos de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ GetItem.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- LVM_GETITEM controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061834"
---
# <a name="lvm_getitem-message"></a>Mensaje \_ GETITEM de LVM

Recupera algunos o todos los atributos de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ GetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que especifica la información que se debe recuperar y recibe información sobre el elemento de vista de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Observaciones

Cuando se envía el mensaje **\_ LVM GETITEM,** los miembros **iItem** e **iSubItem** identifican el elemento o subelemento sobre el que recuperar información y el miembro **mask** especifica qué atributos recuperar. Para obtener una lista de los valores posibles, vea la descripción de la [**estructura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

Si la marca LVIF TEXT se establece en el miembro mask de la estructura \_ [**LVITEM,**](/windows/win32/api/commctrl/ns-commctrl-lvitema) el miembro **pszText** debe apuntar a un búfer válido y el miembro **cchTextMax** debe establecerse en el número de caracteres de ese búfer.  Las aplicaciones no deben suponer que el texto se colocará necesariamente en el búfer especificado. En su lugar, el control puede cambiar el **miembro pszText** de la estructura para que apunte al texto nuevo, en lugar de colocarlo en el búfer.

Si el **miembro mask** especifica el valor LVIF \_ STATE, el miembro **stateMask** debe especificar los bits de estado del elemento que se recuperarán. En la salida, el **miembro de** estado contiene los valores de los bits de estado especificados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ GETITEMW** (Unicode) y **LVM \_ GETITEMA** (ANSI)<br/>                   |



 

 





