---
title: Mensaje de EM_SETREADONLY (Winuser. h)
description: Establece o quita el estilo de solo lectura (ES \_ ReadOnly) de un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETREADONLY controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150230"
---
# <a name="em_setreadonly-message"></a>\_Mensaje SETREADONLY em

Establece o quita el estilo de solo lectura ([**es \_ ReadOnly**](edit-control-styles.md)) de un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si se debe establecer o quitar el estilo [**es de \_ solo lectura**](edit-control-styles.md) . Un valor de **true** establece el estilo **es de \_ solo lectura** ; un valor de **false** quita el estilo **es de \_ solo lectura** .

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Cuando un control de edición tiene el estilo [**es de \_ solo lectura**](edit-control-styles.md) , el usuario no puede cambiar el texto dentro del control de edición.

Para determinar si un control de edición tiene el estilo [**es de \_ solo lectura**](edit-control-styles.md) , use la función [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con la \_ marca de estilo GWL.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

