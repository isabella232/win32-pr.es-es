---
title: EM_GETMODIFY mensaje (Winuser.h)
description: Obtiene el estado de la marca de modificación de un control de edición. La marca indica si se ha modificado el contenido del control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- EM_GETMODIFY controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34156e363824e975af68449b40ed639eeeb7e3ab76bd680b9837f3d3dd907537
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048905"
---
# <a name="em_getmodify-message"></a>Mensaje \_ EM GETMODIFY

Obtiene el estado de la marca de modificación de un control de edición. La marca indica si se ha modificado el contenido del control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ha modificado el contenido del control de edición, el valor devuelto es distinto de cero; de lo contrario, es cero.

## <a name="remarks"></a>Comentarios

El sistema borra automáticamente la marca de modificación en cero cuando se crea el control. Si el usuario cambia el texto del control, el sistema establece la marca en distinto de cero. Puede enviar el mensaje [**EM \_ SETMODIFY al**](em-setmodify.md) control de edición para establecer o borrar la marca.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ SETMODIFY**](em-setmodify.md)
</dt> </dl>

 

 





