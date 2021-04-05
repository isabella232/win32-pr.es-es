---
title: Mensaje de LVM_SETITEM (commctrl. h)
description: Establece algunos o todos los atributos de un elemento de vista de lista. También puede enviar LVM \_ SETITEM para establecer el texto de un subelemento. Puede enviar este mensaje explícitamente o mediante la \_ macro SetItem de ListView.
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- LVM_SETITEM controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079135"
---
# <a name="lvm_setitem-message"></a>\_Mensaje SETITEM LVM

Establece algunos o todos los atributos de un elemento de vista de lista. También puede enviar LVM \_ SETITEM para establecer el texto de un subelemento. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que contiene los nuevos atributos de elemento. Los miembros **iItem** y **iSubItem** identifican el elemento o subelemento y el miembro **Mask** especifica los atributos que se van a establecer. Si el miembro **Mask** especifica el \_ valor de texto LVIF, el miembro **miembros pszText** es la dirección de una cadena terminada en NULL y se omite el miembro **cchTextMax** . Si el miembro **Mask** especifica el \_ valor de estado LVIF, el miembro **stateMask** especifica qué Estados de elemento se van a cambiar y el miembro **State** contiene los valores de esos Estados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Para establecer los atributos de un elemento de vista de lista, establezca el miembro **iItem** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) en el índice del elemento y establezca el miembro **iSubItem** en cero. Para un elemento, puede establecer los miembros **State**, **miembros pszText**, **iImage** y **lParam** de la estructura **LVITEM** .

Para establecer el texto de un subelemento, establezca los miembros **iItem** y **iSubItem** para indicar el subelemento específico y use el miembro **miembros pszText** para especificar el texto. Como alternativa, puede usar la macro [**\_ SetItemText de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) para establecer el texto de un subelemento. No se pueden establecer los miembros **State** o **lParam** para los subelementos porque los subelementos no tienen estos atributos. En la versión 4,70 y posteriores, puede establecer el miembro **iImage** para los subelementos. La imagen del subelemento se mostrará si el control de vista de lista tiene el estilo extendido [**LVS \_ ex \_ SUBITEMIMAGES**](extended-list-view-styles.md) . Las versiones anteriores omitirán la imagen del subelemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ SETITEMW** (Unicode) y **\_ SETITEMA de LVM** (ANSI)<br/>                   |



 

 





