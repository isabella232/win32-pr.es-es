---
title: EM_GETSEL mensaje (Winuser.h)
description: Obtiene las posiciones de caracteres inicial y final (en TCHAR) de la selección actual en un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETSEL de mensajes Windows controles
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca5f3cf1fdaa3c40dd1bb25ebbabb672474e76ae621a05cf52247c216adca17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048805"
---
# <a name="em_getsel-message"></a>Mensaje \_ EM GETSEL

Obtiene las posiciones de caracteres inicial y final (en **TCHAR)** de la selección actual en un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a un **valor DWORD** que recibe la posición inicial de la selección. Este parámetro puede ser **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un **valor DWORD** que recibe la posición del primer carácter no seleccionado después del final de la selección. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un valor de base cero con la posición inicial de la selección en [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y la posición del primer **TCHAR** después del último **TCHAR** seleccionado en [**HIWORD.**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Si alguno de estos valores supera 65 535, el valor devuelto es -1.

Es mejor usar los valores devueltos en *wParam* y *lParam* porque son valores completos de 32 bits.

## <a name="remarks"></a>Comentarios

Si no hay ninguna selección, los valores inicial y final son la posición del cursor de cursor.

**Controles de edición enriquecciones:** También puede usar el mensaje [**EM \_ EXGETSEL**](em-exgetsel.md) para recuperar la misma información. **EM \_ EXGETSEL también** devuelve posiciones de caracteres iniciales y finales como valores de 32 bits.

**Edición enriqueceda:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ EXGETSEL**](em-exgetsel.md)
</dt> <dt>

[**EM \_ SETSEL**](em-setsel.md)
</dt> </dl>

 

