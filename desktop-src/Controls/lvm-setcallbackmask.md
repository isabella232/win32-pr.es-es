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
ms.openlocfilehash: ef6dd46228c4e4aeada30f469a77f9e67aff3a37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061796"
---
# <a name="lvm_setcallbackmask-message"></a>Mensaje \_ LVM SETCALLBACKMASK

Cambia la máscara de devolución de llamada para un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ SetCallbackMask.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de la máscara de devolución de llamada. Los bits de la máscara indican los estados de elemento o las imágenes para las que la aplicación almacena los datos de estado actuales. Este valor puede ser cualquier combinación de las siguientes constantes:



| Value                                                                                                                                                                           | Significado                                                                                            |
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

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Observaciones

La *máscara de devolución* de llamada de un control de vista de lista es un conjunto de marcas de bits que especifican los estados de elemento para los que la aplicación, en lugar del control , almacena los datos actuales. La máscara de devolución de llamada se aplica a todos los elementos del control, a diferencia de la designación de elementos de devolución de llamada, que se aplica a un elemento específico. La máscara de devolución de llamada es cero de forma predeterminada, lo que significa que el control de vista de lista almacena toda la información de estado del elemento. Después de crear un control de vista de lista e inicializar sus elementos, puede enviar el mensaje **\_ LVM SETCALLBACKMASK** para cambiar la máscara de devolución de llamada. Para recuperar la máscara de devolución de llamada actual, envíe el [**mensaje \_ LVM GETCALLBACKMASK.**](lvm-getcallbackmask.md)

Para obtener más información sobre las imágenes superpuestas y las imágenes de estado, vea [Adding List-View Image Lists](using-list-view-controls.md).

Para obtener más información sobre las devoluciones de llamada de vista de lista, vea Elementos de devolución de [llamada y Máscara de devolución de llamada](list-view-controls-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LVN \_ GETDISPINFO**](lvn-getdispinfo.md)
</dt> </dl>

 

 





