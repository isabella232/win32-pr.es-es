---
title: Mensaje de EM_SETMODIFY (Winuser. h)
description: Establece o borra la marca de modificación de un control de edición. La marca de modificación indica si se ha modificado el texto del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_SETMODIFY controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905362"
---
# <a name="em_setmodify-message"></a>\_Mensaje SETMODIFY em

Establece o borra la marca de modificación de un control de edición. La marca de modificación indica si se ha modificado el texto del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Nuevo valor para la marca de modificación. Un valor de **true** indica que el texto se ha modificado y el valor **false** indica que no se ha modificado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El sistema borra automáticamente la marca de modificación a cero cuando se crea el control. Si el usuario cambia el texto del control, el sistema establece la marca en un valor distinto de cero. Puede enviar el mensaje [**\_ GETMODIFY em**](em-getmodify.md) al control de edición para recuperar el estado actual de la marca.

**Rich Edit 1,0:** Los objetos creados sin la marca **reo de \_ Dynamics** se bloquearán en sus extensiones cuando la marca de modificación esté establecida en **false**.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_GETMODIFY em**](em-getmodify.md)
</dt> <dt>

[**Reobject**](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





