---
title: Mensaje de LVM_GETITEMSTATE (commctrl. h)
description: Recupera el estado de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemState de ListView.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- LVM_GETITEMSTATE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492412"
---
# <a name="lvm_getitemstate-message"></a>\_Mensaje GETITEMSTATE LVM

Recupera el estado de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemState de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Información de estado que se va a recuperar. Este parámetro puede ser una combinación de los siguientes valores:



| Value                                                                                                                                                                           | Significado                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ cortar**</dt> </dl>                                  | El elemento está marcado para una operación de cortar y pegar.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | El elemento se resalta como un destino de arrastrar y colocar.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ centrado**</dt> </dl>                      | El elemento tiene el foco, por lo que está rodeado por un rectángulo de foco estándar. Aunque se puede seleccionar más de un elemento, solo un elemento puede tener el foco.<br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ seleccionado**</dt> </dl>                   | El elemento está seleccionado. La apariencia de un elemento seleccionado depende de si tiene el foco y también de los colores del sistema utilizados para la selección.<br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | Use esta máscara para recuperar el índice de la imagen de superposición del elemento.<br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | Use esta máscara para recuperar el índice de imagen de estado del elemento.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el estado actual del elemento especificado. Los únicos bits válidos en el valor devuelto son los que corresponden a los bits establecidos en el parámetro *lParam* .

## <a name="remarks"></a>Observaciones

La información de estado de un elemento incluye un conjunto de marcas de bits, así como índices de lista de imágenes que indican la imagen de estado del elemento y la imagen de superposición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETITEMSTATE LVM**](lvm-setitemstate.md)
</dt> </dl>

 

 





