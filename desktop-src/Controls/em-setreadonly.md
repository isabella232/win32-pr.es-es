---
title: EM_SETREADONLY mensaje (Winuser.h)
description: Establece o quita el estilo de solo lectura (ES \_ READONLY) de un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETREADONLY controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062073"
---
# <a name="em_setreadonly-message"></a>Mensaje \_ EM SETREADONLY

Establece o quita el estilo de solo lectura [**(ES \_ READONLY)**](edit-control-styles.md)de un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si se debe establecer o quitar el [**estilo ES \_ READONLY.**](edit-control-styles.md) Un valor **true establece** el estilo ES **\_ READONLY;** un valor **de FALSE** quita el estilo ES **\_ READONLY.**

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Cuando un control de edición tiene el estilo [**ES \_ READONLY,**](edit-control-styles.md) el usuario no puede cambiar el texto dentro del control de edición.

Para determinar si un control de edición tiene el estilo [**ES \_ READONLY,**](edit-control-styles.md) use la [**función GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con la marca GWL \_ STYLE.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

