---
title: LVM_SETITEM mensaje (Commctrl.h)
description: Establece algunos o todos los atributos de un elemento de vista de lista. También puede enviar LVM \_ SETITEM para establecer el texto de un subelemento. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ SetItem.
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- LVM_SETITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362707"
---
# <a name="lvm_setitem-message"></a>Mensaje \_ SETITEM de LVM

Establece algunos o todos los atributos de un elemento de vista de lista. También puede enviar LVM \_ SETITEM para establecer el texto de un subelemento. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que contiene los nuevos atributos de elemento. Los **miembros iItem** **e iSubItem** identifican el elemento o subelemento, y el miembro **mask** especifica qué atributos se deben establecer. Si el **miembro mask** especifica el valor LVIF TEXT, el miembro pszText es la dirección de una cadena terminada en NULL y el miembro \_ **cchTextMax** se omite.  Si el **miembro mask** especifica el valor LVIF STATE, el miembro \_ **stateMask** especifica qué estados de elemento se deben cambiar y el miembro de estado contiene los valores para esos estados. 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

Para establecer los atributos de un elemento de vista de lista, establezca el miembro **iItem** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) en el índice del elemento y establezca el miembro **iSubItem** en cero. Para un elemento, puede establecer los miembros **de** estado , **pszText**, **iImage** y **lParam** de la **estructura LVITEM.**

Para establecer el texto de un subelemento, establezca los miembros **iItem** e **iSubItem** para indicar el subelemento específico y use el miembro **pszText** para especificar el texto. Como alternativa, puede usar la macro [**\_ ListView SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) para establecer el texto de un subelemento. No se puede establecer **el estado o** los miembros **lParam** para los subelementos porque los subelementos no tienen estos atributos. En la versión 4.70 y posteriores, puede establecer el miembro **iImage** para los subelementos. La imagen de subelemento se mostrará si el control list-view tiene el estilo [**extendido LVS \_ EX \_ SUBITEMIMAGES.**](extended-list-view-styles.md) Las versiones anteriores omitirán la imagen de subelemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ SETITEMW** (Unicode) y **LVM \_ SETITEMA** (ANSI)<br/>                   |



 

 





