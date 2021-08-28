---
title: EM_GETLINE mensaje (Winuser.h)
description: Copia una línea de texto de un control de edición y lo coloca en un búfer especificado. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETLINE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4398fa27acf6d70d100c4aa98a1e06c2d6685b7a06cf6effc7e0666bbd6a1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006698"
---
# <a name="em_getline-message-winuserh"></a>EM_GETLINE mensaje (Winuser.h)

Copia una línea de texto de un control de edición y lo coloca en un búfer especificado. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la línea que se recupera de un control de edición multilínea. Un valor de cero especifica la línea superior. Un control de edición de una sola línea omite este parámetro.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibe una copia de la línea. Antes de enviar el mensaje, establezca la primera palabra de este búfer en el tamaño, en **TCHAR,** del búfer. En el caso del texto ANSI, este es el número de bytes; para texto Unicode, este es el número de caracteres. La línea copiada sobrescribe el tamaño de la primera palabra.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el número de **TCHAR** copiados. El valor devuelto es cero si el número de línea especificado por el *parámetro wParam* es mayor que el número de líneas del control de edición.

## <a name="remarks"></a>Comentarios

**Editar controles:** La línea copiada no contiene un carácter nulo de terminación.

**Controles de edición enriquecciones:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. La línea copiada no contiene un carácter nulo de terminación, a menos que no se copie ningún texto. Si no se ha copiado ningún texto, el mensaje coloca un carácter nulo al principio del búfer. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ LINELENGTH**](em-linelength.md)
</dt> <dt>

[**Editar \_ GetLine**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

