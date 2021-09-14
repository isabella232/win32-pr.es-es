---
title: LVM_GETITEMSTATE mensaje (Commctrl.h)
description: Recupera el estado de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetItemState.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- LVM_GETITEMSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b355e78f22c01c289f681d256ee6b4d0aa882
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974087"
---
# <a name="lvm_getitemstate-message"></a>Mensaje GETITEMSTATE de LVM \_

Recupera el estado de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetItemState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento list-view.

</dd> <dt>

*lParam* 
</dt> <dd>

Información de estado que se recuperará. Este parámetro puede ser una combinación de los valores siguientes:



| Value                                                                                                                                                                           | Significado                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ CUT**</dt> </dl>                                  | El elemento está marcado para una operación de cortar y pegar.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | El elemento se resalta como un destino de arrastrar y colocar.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ CENTRADO**</dt> </dl>                      | El elemento tiene el foco, por lo que está rodeado por un rectángulo de foco estándar. Aunque se puede seleccionar más de un elemento, solo un elemento puede tener el foco.<br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ SELECCIONADO**</dt> </dl>                   | El elemento está seleccionado. La apariencia de un elemento seleccionado depende de si tiene el foco y también de los colores del sistema usados para la selección.<br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**SUPERPOSICIÓN \_ DE LVISMASK**</dt> </dl>          | Use esta máscara para recuperar el índice de imagen superpuesta del elemento.<br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | Use esta máscara para recuperar el índice de imagen de estado del elemento.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el estado actual del elemento especificado. Los únicos bits válidos del valor devuelto son los que corresponden a los bits establecidos en el *parámetro lParam.*

## <a name="remarks"></a>Observaciones

La información de estado de un elemento incluye un conjunto de marcas de bits, así como índices de lista de imágenes que indican la imagen de estado y la imagen de superposición del elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LVM \_ SETITEMSTATE**](lvm-setitemstate.md)
</dt> </dl>

 

 





