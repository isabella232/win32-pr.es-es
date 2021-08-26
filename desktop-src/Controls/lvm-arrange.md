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
ms.openlocfilehash: 98d7e3595c276815af8708a54d6e81c2a40192d8d07e6cbce514481723799d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062655"
---
# <a name="lvm_arrange-message"></a>Mensaje \_ DE LVM ARRANGE

Organiza los elementos en la vista de iconos. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ Arrange.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uno de los siguientes valores que especifica la alineación:



| Value                                                                                                                                                            | Significado                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <dt>**LVA \_ ALIGNLEFT**</dt> </dl>    | Sin implementar. En su [**lugar, aplique \_ el estilo LVS ALIGNLEFT.**](list-view-window-styles.md)<br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <dt>**LVA \_ ALIGNTOP**</dt> </dl>       | Sin implementar. En su [**lugar, aplique \_ el estilo LVS ALIGNTOP.**](list-view-window-styles.md)<br/>   |
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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





