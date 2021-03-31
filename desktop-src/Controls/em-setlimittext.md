---
title: Mensaje de EM_SETLIMITTEXT (Winuser. h)
description: Establece el límite de texto de un control de edición.
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- EM_SETLIMITTEXT controles de mensajes de Windows
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
ms.openlocfilehash: 5c138e6d7fed75fa8da2e7a6b93308632c250e7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802654"
---
# <a name="em_setlimittext-message"></a>\_Mensaje SETLIMITTEXT em

Establece el límite de texto de un control de edición. El límite de texto es la cantidad máxima de texto, en **TCHAR** s, que el usuario puede escribir en el control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

En el caso de los controles de edición y Microsoft Rich Edit 1,0, se usan bytes. En el caso de Microsoft Rich Edit 2,0 y versiones posteriores, se usan caracteres.

El mensaje **em \_ SETLIMITTEXT** es idéntico al mensaje [**\_ LIMITTEXT em**](em-limittext.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El número máximo de **TCHAR** s que el usuario puede escribir. Para texto ANSI, es el número de bytes; en el caso de texto Unicode, es el número de caracteres. Este número no incluye el carácter nulo de terminación.

**Controles Rich Edit:** Si este parámetro es cero, la longitud del texto se establece en 64.000 caracteres.

Si este parámetro es cero, la longitud del texto se establece en 0x7FFFFFFE caracteres para los controles de edición de una sola línea o en 1 para los controles de edición multilínea.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El **mensaje \_ SETLIMITTEXT em** limita solo el texto que el usuario puede escribir. No afecta a ningún texto que ya esté en el control de edición cuando se envía el mensaje, ni afecta a la longitud del texto copiado en el control de edición por el mensaje de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) . Si una aplicación utiliza el mensaje de **WM \_ SETTEXT** para colocar más texto en un control de edición que se especifica en el mensaje **\_ SETLIMITTEXT em** , el usuario puede editar todo el contenido del control de edición.

Antes de que se llame a **em \_ SETLIMITTEXT** , el límite predeterminado para la cantidad de texto que un usuario puede escribir en un control de edición es de 32.767 caracteres.

En el caso de los controles de edición de una sola línea, el límite del texto es 0x7FFFFFFE bytes o el valor del parámetro *wParam* , el que sea menor. En el caso de los controles de edición multilínea, este valor es 1 bytes o el valor del parámetro *wParam* , el que sea menor.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Use el mensaje [**em \_ EXLIMITTEXT**](em-exlimittext.md) para valores de longitud de texto mayor que 64.000. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETLIMITTEXT em**](em-getlimittext.md)
</dt> </dl>

 

