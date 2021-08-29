---
title: EM_SETLIMITTEXT mensaje (Winuser.h)
description: 'EM_SETLIMITTEXT mensaje: establece el límite de texto de un control de edición.'
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- EM_SETLIMITTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98105c3384c2f218c13ad39da7be0828a601e8d3e166edbf2e3ef02553cf88de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437537"
---
# <a name="em_setlimittext-message"></a>Mensaje \_ EM SETLIMITTEXT

Establece el límite de texto de un control de edición. El límite de texto es la cantidad máxima de texto, en **TCHAR,** que el usuario puede escribir en el control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

Para los controles de edición y Microsoft Rich Edit 1.0, se usan bytes. Para Microsoft Rich Edit 2.0 y versiones posteriores, se usan caracteres.

El **mensaje EM \_ SETLIMITTEXT** es idéntico al mensaje [**EM \_ LIMITTEXT.**](em-limittext.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número máximo de **TCHAR** que el usuario puede especificar. Para el texto ANSI, este es el número de bytes; Para el texto Unicode, este es el número de caracteres. Este número no incluye el carácter nulo de terminación.

**Controles de edición enriquecciones:** Si este parámetro es cero, la longitud del texto se establece en 64 000 caracteres.

Si este parámetro es cero, la longitud del texto se establece en 0x7FFFFFFE para los controles de edición de una sola línea o 1 para los controles de edición multilínea.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

El **mensaje EM \_ SETLIMITTEXT** limita solo el texto que el usuario puede escribir. No afecta a ningún texto que ya esté en el control de edición cuando se envía el mensaje, ni afecta a la longitud del texto copiado en el control de edición por el mensaje [**\_ SETTEXT de WM.**](/windows/desktop/winmsg/wm-settext) Si una aplicación usa el mensaje **\_ SETTEXT** de WM para colocar más texto en un control de edición que el especificado en el mensaje **EM \_ SETLIMITTEXT,** el usuario puede editar todo el contenido del control de edición.

Antes de llamar a **EM \_ SETLIMITTEXT,** el límite predeterminado para la cantidad de texto que un usuario puede escribir en un control de edición es de 32 767 caracteres.

Para los controles de edición de una sola línea, el límite de texto es 0x7FFFFFFE bytes o el valor del parámetro *wParam,* lo que sea menor. Para los controles de edición multilínea, este valor es de 1 bytes o el valor del parámetro *wParam,* lo que sea menor.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Use el mensaje [**EM \_ EXLIMITTEXT para**](em-exlimittext.md) valores de longitud de texto mayores que 64 000. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ GETLIMITTEXT**](em-getlimittext.md)
</dt> </dl>

 

