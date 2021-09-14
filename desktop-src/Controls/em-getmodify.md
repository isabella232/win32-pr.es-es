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
ms.openlocfilehash: 4f8c525df061717255051c49abaa3bda88f317b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170070"
---
# <a name="em_getmodify-message"></a>Mensaje \_ GETMODIFY DE EM

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

## <a name="remarks"></a>Observaciones

El sistema borra automáticamente la marca de modificación en cero cuando se crea el control. Si el usuario cambia el texto del control, el sistema establece la marca en distinto de cero. Puede enviar el mensaje [**EM \_ SETMODIFY**](em-setmodify.md) al control de edición para establecer o borrar la marca.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ SETMODIFY**](em-setmodify.md)
</dt> </dl>

 

 





