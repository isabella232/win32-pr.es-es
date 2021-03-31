---
title: Mensaje de LVM_ARRANGE (commctrl. h)
description: Organiza los elementos en la vista de iconos. Puede enviar este mensaje explícitamente o mediante la \_ macro Arrange de ListView.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- LVM_ARRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149908"
---
# <a name="lvm_arrange-message"></a>Mensaje de organización del LVM \_

Organiza los elementos en la vista de iconos. Puede enviar este mensaje explícitamente o mediante la macro [**\_ Arrange de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uno de los siguientes valores que especifica la alineación:



| Value                                                                                                                                                            | Significado                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <dt>**LVA \_ ALIGNLEFT**</dt> </dl>    | Sin implementar. Aplique el [**estilo \_ ALIGNLEFT LVS**](list-view-window-styles.md) en su lugar.<br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <dt>**LVA \_ ALIGNTOP**</dt> </dl>       | Sin implementar. Aplique el [**estilo \_ ALIGNTOP LVS**](list-view-window-styles.md) en su lugar.<br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <dt>**\_valor predeterminado de LVA**</dt> </dl>          | Alinea los elementos según los estilos de alineación actual del control de vista de lista (valor predeterminado).<br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <dt>**LVA \_ SNAPTOGRID**</dt> </dl> | Ajusta todos los iconos a la posición de la cuadrícula más cercana.<br/>                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true si es** correcto; en caso contrario, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





