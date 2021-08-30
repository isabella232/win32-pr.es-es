---
title: TVM_SELECTITEM mensaje (Commctrl.h)
description: Selecciona el elemento de vista de árbol especificado, desplaza el elemento a la vista o vuelve a dibujar el elemento en el estilo utilizado para indicar el destino de una operación de arrastrar y colocar.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- TVM_SELECTITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec7201358669fa49e6396508d371ca5e95d6fa1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472961"
---
# <a name="tvm_selectitem-message"></a>Mensaje \_ SELECTITEM de TVM

Selecciona el elemento de vista de árbol especificado, desplaza el elemento a la vista o vuelve a dibujar el elemento en el estilo utilizado para indicar el destino de una operación de arrastrar y colocar. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)o [**TreeView \_ SelectDropTarget.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca de acción. Este parámetro puede ser uno de los siguientes valores:




| Valor | Significado | 
|-------|---------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl><dt><strong>TVGN_CARET</strong></dt></dl> | Establece la selección en el elemento especificado. La ventana primaria del control de vista de árbol recibe los <a href="tvn-selchanging.md">TVN_SELCHANGING</a> y <a href="tvn-selchanged.md">TVN_SELCHANGED</a> de notificación. <br /> | 
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl><dt><strong>TVGN_DROPHILITE</strong></dt></dl> | Vuelve a dibujar el elemento especificado en el estilo utilizado para indicar el destino de una operación de arrastrar y colocar.<br /> | 
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl><dt><strong>TVGN_FIRSTVISIBLE</strong></dt></dl> | Garantiza que el elemento especificado está visible y, si es posible, lo muestra en la parte superior de la ventana del control. Los controles de vista de árbol muestran tantos elementos como quepa en la ventana. Si el elemento especificado está cerca de la parte inferior de la jerarquía de elementos del control, es posible que no se convierta en el primer elemento visible, en función del número de elementos que quepa en la ventana.<br /> | 
| <span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt></dl> | Cuando se selecciona un solo elemento, se asegura de que la vista de árbol no expande los elementos secundarios de ese elemento. Esto solo es válido si se usa con TVGN_CARET marca. <br /><blockquote>[!Note]<br />Para usar esta marca, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">Habilitar estilos visuales.</a></blockquote><br /> | 




 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de un elemento. Si *lParam es* **NULL,** el control se establece para que no tenga ningún elemento seleccionado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

Si el elemento especificado es el elemento secundario de un elemento primario contraído, la lista de elementos secundarios del elemento primario se expande para mostrar el elemento especificado. En este caso, la ventana primaria del control recibe los códigos de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED.](tvn-itemexpanded.md)

El uso de la macro [**\_ TreeView SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) equivale a enviar el mensaje **\_ SELECTITEM** de TVM con *wParam* establecido en el \_ valor DE TVGN CARET. El uso de la macro [**\_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) de TreeView equivale a enviar el mensaje **\_ SELECTITEM** de TVM con *wParam* establecido en el valor \_ DROPHILITE de TVGN. El [**uso de TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) equivale a enviar el mensaje **\_ SELECTITEM** de TVM con *wParam* establecido en el valor TVGN \_ FIRSTVISIBLE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





