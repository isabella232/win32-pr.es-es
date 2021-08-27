---
title: LVM_SETCALLBACKMASK mensaje (Commctrl.h)
description: Cambia la máscara de devolución de llamada para un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ SetCallbackMask.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- LVM_SETCALLBACKMASK controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79e33b106eb0c59f83e40b9f170dd017fcdda412072ed51a26572fcf368f5215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088855"
---
# <a name="lvm_setcallbackmask-message"></a>Mensaje \_ SETCALLBACKMASK de LVM

Cambia la máscara de devolución de llamada para un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ SetCallbackMask.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de la máscara de devolución de llamada. Los bits de la máscara indican los estados o imágenes de los elementos para los que la aplicación almacena los datos de estado actuales. Este valor puede ser cualquier combinación de las siguientes constantes:



| Valor                                                                                                                                                                           | Significado                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ CUT**</dt> </dl>                                  | El elemento está marcado para una operación de cortar y pegar.<br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | El elemento se resalta como un destino de arrastrar y colocar.<br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ CENTRADO**</dt> </dl>                      | El elemento tiene el foco.<br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ SELECCIONADO**</dt> </dl>                   | El elemento está seleccionado. <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**SUPERPOSICIÓN \_ DE LVISMASK**</dt> </dl>          | La aplicación almacena el índice de la lista de imágenes de la imagen superpuesta actual para cada elemento.<br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | La aplicación almacena el índice de la lista de imágenes de la imagen de estado actual para cada elemento. <br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

La *máscara de devolución* de llamada de un control de vista de lista es un conjunto de marcas de bits que especifican los estados de elemento para los que la aplicación, en lugar del control , almacena los datos actuales. La máscara de devolución de llamada se aplica a todos los elementos del control, a diferencia de la designación del elemento de devolución de llamada, que se aplica a un elemento específico. La máscara de devolución de llamada es cero de forma predeterminada, lo que significa que el control list-view almacena toda la información de estado del elemento. Después de crear un control de vista de lista e inicializar sus elementos, puede enviar el mensaje **LVM \_ SETCALLBACKMASK** para cambiar la máscara de devolución de llamada. Para recuperar la máscara de devolución de llamada actual, envíe el [**mensaje \_ LVM GETCALLBACKMASK.**](lvm-getcallbackmask.md)

Para obtener más información sobre las imágenes de superposición y las imágenes de estado, vea [Adding List-View Image Lists](using-list-view-controls.md).

Para obtener más información sobre las devoluciones de llamada de vista de lista, vea Elementos de devolución de [llamada y máscara de devolución de llamada](list-view-controls-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LVN \_ GETDISPINFO**](lvn-getdispinfo.md)
</dt> </dl>

 

 





