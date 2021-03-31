---
title: Mensaje de EM_GETMODIFY (Winuser. h)
description: Obtiene el estado de la marca de modificación de un control de edición. La marca indica si se ha modificado el contenido del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- EM_GETMODIFY controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905060"
---
# <a name="em_getmodify-message"></a>\_Mensaje GETMODIFY em

Obtiene el estado de la marca de modificación de un control de edición. La marca indica si se ha modificado el contenido del control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ha modificado el contenido del control de edición, el valor devuelto es distinto de cero; de lo contrario, es cero.

## <a name="remarks"></a>Observaciones

El sistema borra automáticamente la marca de modificación a cero cuando se crea el control. Si el usuario cambia el texto del control, el sistema establece la marca en un valor distinto de cero. Puede enviar el mensaje [**\_ SETMODIFY em**](em-setmodify.md) al control Editar para establecer o borrar la marca.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETMODIFY em**](em-setmodify.md)
</dt> </dl>

 

 





