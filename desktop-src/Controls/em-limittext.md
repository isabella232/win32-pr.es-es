---
title: EM_LIMITTEXT mensaje (Winuser.h)
description: 'EM_LIMITTEXT mensaje: establece el límite de texto de un control de edición.'
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- EM_LIMITTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80ce29d4ee5155f6b3c5c32609366982655a078
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062171"
---
# <a name="em_limittext-message"></a>Mensaje \_ DE EM LIMITTEXT

Establece el límite de texto de un control de edición. El límite de texto es la cantidad máxima de texto, en **TCHAR,** que el usuario puede escribir en el control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

Para los controles de edición y Microsoft Rich Edit 1.0, se usan bytes. Para Microsoft Rich Edit 2.0 y versiones posteriores, se usan caracteres.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número máximo de **TCHAR que** el usuario puede especificar. Para el texto ANSI, este es el número de bytes; Para el texto Unicode, este es el número de caracteres. Este número no incluye el carácter nulo de terminación.

**Controles de edición enriquecciones:** Si este parámetro es cero, la longitud del texto se establece en 64 000 caracteres.

Si este parámetro es cero, la longitud del texto se establece en 0x7FFFFFFE para los controles de edición de una sola línea o -1 para los controles de edición multilínea.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

El **mensaje EM \_ LIMITTEXT** limita solo el texto que el usuario puede escribir. No afecta a ningún texto que ya esté en el control de edición cuando se envía el mensaje, ni afecta a la longitud del texto copiado en el control de edición por el mensaje [**\_ SETTEXT de WM.**](/windows/desktop/winmsg/wm-settext) Si una aplicación usa el mensaje **\_ WM SETTEXT** para colocar más texto en un control de edición que el especificado en el mensaje **EM \_ LIMITTEXT,** el usuario puede editar todo el contenido del control de edición.

Antes de llamar a **EM \_ LIMITTEXT,** el límite predeterminado para la cantidad de texto que un usuario puede escribir en un control de edición es de 32 767 caracteres.

Para los controles de edición de una sola línea, el límite de texto es 0x7FFFFFFE bytes o el valor del parámetro *wParam,* lo que sea menor. Para los controles de edición multilínea, este valor es -1 byte o el valor del parámetro *wParam,* lo que sea menor.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Use el mensaje [**EM \_ EXLIMITTEXT para**](em-exlimittext.md) valores de longitud de texto mayores que 64 000. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

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

[**EM \_ EXLIMITTEXT**](em-exlimittext.md)
</dt> <dt>

[**Editar \_ LimitText**](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

