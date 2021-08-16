---
title: EM_GETLIMITTEXT mensaje (Winuser.h)
description: Obtiene el límite de texto actual para un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- EM_GETLIMITTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2066bf03fd8ea05851a9cef58f4e308db49f82bdee94c2d503cadf1c20a2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831686"
---
# <a name="em_getlimittext-message"></a>Mensaje \_ EM GETLIMITTEXT

Obtiene el límite de texto actual para un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

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

El valor devuelto es el límite de texto.

## <a name="remarks"></a>Comentarios

**Editar controles, Rich Edit 2.0 y versiones posteriores:** El límite de texto es la cantidad máxima de texto, en **TCHAR,** que el control puede contener. En el caso del texto ANSI, este es el número de bytes; para texto Unicode, este es el número de caracteres. Dos documentos con el mismo límite de caracteres darán como resultado el mismo límite de texto, incluso si uno es ANSI y el otro es Unicode.

**Rich Edit 1.0:** El límite de texto es la cantidad máxima de texto, en bytes, que puede contener el control de edición enriquecido.

**Edición enriqueceda:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ SETLIMITTEXT**](em-setlimittext.md)
</dt> </dl>

 

 





