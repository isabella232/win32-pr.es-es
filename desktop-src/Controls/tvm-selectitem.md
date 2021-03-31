---
title: Mensaje de TVM_SELECTITEM (commctrl. h)
description: Selecciona el elemento de vista de árbol especificado, desplaza el elemento a la vista o vuelve a dibujar el elemento en el estilo utilizado para indicar el destino de una operación de arrastrar y colocar.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- TVM_SELECTITEM controles de mensajes de Windows
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
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905080"
---
# <a name="tvm_selectitem-message"></a>\_Mensaje de SELECTITEM TVM

Selecciona el elemento de vista de árbol especificado, desplaza el elemento a la vista o vuelve a dibujar el elemento en el estilo utilizado para indicar el destino de una operación de arrastrar y colocar. Puede enviar este mensaje explícitamente o mediante la macro [**\_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)o [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) de TreeView.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca de acción. Este parámetro puede ser uno de los siguientes valores:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt><strong>TVGN_CARET</strong></dt> </dl></td>
<td>Establece la selección en el elemento especificado. La ventana primaria del control de vista de árbol recibe los códigos de notificación de <a href="tvn-selchanging.md">TVN_SELCHANGING</a> y <a href="tvn-selchanged.md">TVN_SELCHANGED</a> . <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt><strong>TVGN_DROPHILITE</strong></dt> </dl></td>
<td>Vuelve a dibujar el elemento especificado en el estilo utilizado para indicar el destino de una operación de arrastrar y colocar.<br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </dl></td>
<td>Garantiza que el elemento especificado esté visible y, si es posible, lo muestra en la parte superior de la ventana del control. Los controles de vista de árbol muestran tantos elementos como quepan en la ventana. Si el elemento especificado está cerca de la parte inferior de la jerarquía de elementos del control, puede que no se convierta en el primer elemento visible, en función de cuántos elementos quepan en la ventana.<br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </dl></td>
<td>Cuando se selecciona un solo elemento, garantiza que la vista de árbol no expande los elementos secundarios de ese elemento. Esto solo es válido si se usa con la marca TVGN_CARET. <br/>
<blockquote>
[!Note]<br />
Para usar esta marca, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">habilitar estilos visuales</a>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de un elemento. Si *lParam* es **null**, el control se establece para que no tenga ningún elemento seleccionado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Si el elemento especificado es el elemento secundario de un elemento primario contraído, la lista de elementos secundarios del elemento primario se expande para mostrar el elemento especificado. En este caso, la ventana primaria del control recibe los códigos de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .

Usar la [**macro \_ SelectItem de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) es equivalente a enviar el mensaje **TVM \_ SelectItem** con *wParam* establecido en el \_ valor del símbolo de intercalación TVGN. Usar la [**macro \_ SelectDropTarget de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) es equivalente a enviar el mensaje **TVM \_ SELECTITEM** con *wParam* establecido en el \_ valor de TVGN DROPHILITE. El uso de [**TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) es equivalente a enviar el mensaje **TVM \_ SELECTITEM** con *wParam* establecido en el valor de TVGN \_ FIRSTVISIBLE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





