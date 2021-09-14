---
title: EM_SETMODIFY mensaje (Winuser.h)
description: Establece o borra la marca de modificación de un control de edición. La marca de modificación indica si se ha modificado el texto del control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_SETMODIFY controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062090"
---
# <a name="em_setmodify-message"></a>Mensaje \_ SETMODIFY de EM

Establece o borra la marca de modificación de un control de edición. La marca de modificación indica si se ha modificado el texto del control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Nuevo valor para la marca de modificación. Un valor **true indica** que el texto se ha modificado y un valor **false** indica que no se ha modificado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

El sistema borra automáticamente la marca de modificación en cero cuando se crea el control. Si el usuario cambia el texto del control, el sistema establece la marca en distinto de cero. Puede enviar el mensaje [**EM \_ GETMODIFY**](em-getmodify.md) al control de edición para recuperar el estado actual de la marca.

**Rich Edit 1.0:** Los objetos creados sin **la marca \_ REO DYNAMICSIZE** se bloquearán en sus extensiones cuando la marca modify esté establecida en **FALSE.**

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETMODIFY**](em-getmodify.md)
</dt> <dt>

[**REOBJECT**](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





