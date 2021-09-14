---
title: LVM_ARRANGE mensaje (Commctrl.h)
description: Organiza los elementos en la vista de iconos. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ Arrange.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- LVM_ARRANGE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974106"
---
# <a name="lvm_arrange-message"></a>Mensaje LVM \_ ARRANGE

Organiza los elementos en la vista de iconos. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ Arrange.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uno de los siguientes valores que especifica la alineación:



| Value                                                                                                                                                            | Significado                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <dt>**LVA \_ ALIGNLEFT**</dt> </dl>    | Sin implementar. Aplique el [**estilo \_ ALIGNLEFT de LVS**](list-view-window-styles.md) en su lugar.<br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <dt>**LVA \_ ALIGNTOP**</dt> </dl>       | Sin implementar. Aplique el [**estilo \_ ALIGNTOP de LVS**](list-view-window-styles.md) en su lugar.<br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <dt>**LVA \_ DEFAULT**</dt> </dl>          | Alinea los elementos según los estilos de alineación actuales del control de vista de lista (el valor predeterminado).<br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <dt>**LVA \_ SNAPTOGRID**</dt> </dl> | Ajusta todos los iconos a la posición de cuadrícula más cercana.<br/>                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente; de lo contrario, **FALSE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





